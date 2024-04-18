# Jovan_Lukic_Portfolio

Hi, My name is Jovan Lukic. I'm currently a volunteer 'Robotics Engineer' at a local startup. My current role revolves around software development of an Unmanned Surface Vehicle (USV) used for oceanic cleanup. I'm creating this portfolio to show off my past work as an undergrad, as well as a professional. I like all things engineering, even though my current focus is in robotics i'm open to any and all industries. While I continue my volunteer work, I am looking for a formal position. With that said, for any future employer who is interested in my past/current work feel free to look over this portfolio. I'm am planning on continuing my learning so as I work on my side project, I will update my portfolio accordingly.

# Project 'Cali'

This project is a continuation of 'Project Cali' a mobile manipulator designed by students and staff of California State University Los Angeles (CSULA), and the members of the student organization 'American Society of Mechanical Engineers (ASME). Link: https://github.com/ASME-ground-robot/robot_cali. This platform is intended for reasearch, educational purposes, as well as design competitions. If you would like to read more about the overal project feel free to click on the link provided. I took part in development starting in May 2022, where I acted as a research assistant for a graduate level research, where I worked on developing this controller needed to manipulate the 'Scorbot ER III' robotic arm which was used in development of this platform . I then led further development of 'Project Cali' as a 'Project Lead' from September 2022 - May 2023, where I've done further work in navigation.

# Undergraduate Research 

<ins>Scorbot Controls<ins/>

Between May 2022 - May 2023 I took part in a graduate level research to provide the field of robotics with contribution in regards to 'Mobile Manipulators' and their use in industrial seeting. I initially started my work performing systems level testing, hardware component troubleshooting, and I later on moved to development. My role then turn to creating the necessary controls scheme in order to manipulate a 6-DOF robotic arm the was integrated onto the platform. The specific model that I was working with was a 'Scorbot ER III' robotic arm. After some time, I was able to complete this side of the prokect with my work being presented down below.

Project Link: https://github.com/JovanLukic79/scorbot_control_2


![Rover_Urc](https://github.com/JovanLukic79/scorbot_control_2/assets/115774118/f26800ed-8741-468d-a514-e1811fa5fde4)


This repo describes one of my particular contribution of the overall platform which is to provide a control scheme for the 6-link robotic arm integrated onto the overall platform. ROS's 'MoveIt' package was used to provide the control system, and GUI needed for robotic arm manipulation. ROS version that was used is ROS melodic. With that said, this package provides the code needed to interface ros_control and controllers with any sort of embedded controls. Later I may provide an example of said emedded controls just to demonstrate how this package would communicate with a set of hardware controls to acheive joint articulation. For now, I will just provide this part of the system for anyone who needs it as well as to use as my personal portfolio. This package can also be configured to any general robotic arm, so if you happen to need to interface your hardware controls with ROS's control system, feel free to use this as a template. With that said, a description of this package is provided bellow.


![IMG_1666](https://github.com/JovanLukic79/scorbot_control_2/assets/115774118/0d4ebff5-e54c-4485-bf71-09ed5fdbdc6d)

<ins>Description<ins/>

This repo is made up of two packages. The first one is "scorbot_control_2". This package is where I defined my hardware interface for the robotic arm. In addition to that,"scorbot_control_2" consists of the robotic arm simulation pacakge named "gazebo.launch". The second package is "scorbot_moveit_2", was built using "moveit_setup_assistants". This contains "move_group.launch" the main node needed to communicate with the rest of ROS's control system. In addition to movegroup, this package would also provide moveit_rviz.launch file which woutld act as the main GUI needed to control your robotic arm. 

<ins>Demonstration<ins/>
![robotic_arm_demo](https://github.com/JovanLukic79/scorbot_control_2/assets/115774118/fde7b4bf-d4aa-48ad-9057-2868b8ec43db)


# 'Cali' Outdoor Navigation

Project Link: https://github.com/JovanLukic79/cali_outdoor_nav/blob/main/README.md

As I was participating in research using this platform, I also led a team of 9 (nine) multi-disciplinary engineers in order to have this platform to compete in a student design competion. This was for my Student CAPSTONE project, and I was 'Project Lead'. My technical role was navigation, and I was tasked to develop the navigation system for this particular platform. The goal was for this platform to be able to travesre unknon terrain using GPS odmotery, and I was able to configure localization needed in order to do that. Bellow is the descriptoin of said system.

<ins>Description</ins>

This repo describes one of my particular contribution of the navigation system intended for outdoor navigation. It uses a GPS odometry in order to perform localizastion. The localizzation algorithim that was used was "ekf_localization", from the "robot_localization" package. A 'sensor fusion' based localization algorithim that is able to perform sensor fusion based localizastion using either IMU, Wheel, and GPS odometry to generate 2D-State estimation [2]. In this build, I configured our localization to use GPS, and IMU. "Navsat_transform" algorithim was also used in order to perform the actual sensor fusion, and to turn the GPS/IMU data into "/odometry/fix" messages in order for "ekf_localization" to subscribe too. I added a simulated world 'cpr_orchard_gazebo' provided by 'Clear Path Robotics', in order to simulate 'Cali' robot in an outdoor agricultrual environment. Lastly, sensor models provided by 'Hector_gazebo_pluggins" were provided to simulate GPS,IMU sensor data [5].

I've also created a node that is able to send a waypoint to some specific location using cartesian coordinates. This doesn't serve much purpose but I decided to add it anyways. I also inteded to create my own coverage planner. Since i'm simulating 'Cali' rover in an 'Orchard field', I'd think it would've been fitting for 'Cali' to do some form of sweep/coverage planning. However, I just wanted to have this up so I could finally start doing projects in ROS2. With that said, the extent of this project is just to have 'robot_localization' configured to 'Project Cali', and to have it perform navigation (using '2D Nav goals') on simulation (Considering by the time I had it figured out, I already graduated and don't have access to the phyiscal rover).  

<ins>Dependencies (Install):</ins>
- 'Project Cali' Repo: https://github.com/ASME-ground-robot/robot_cali
- 'Robot_Localization': https://github.com/cra-ros-pkg/robot_localization (git clone) or "sudo apt-get insatll ros-melodic-robot-localization"
- Clear path Robotics 'cpr_orchard_gazebo" simulation world: https://github.com/clearpathrobotics/cpr_gazebo
  
<ins>Demonstration</ins>

<ins>Desclaimer</ins>
I needed to lower the fps, and cut the recorded demonstrations to 30 seconds in order to fit this GIF into this repo.

![Navigation_demo(3)](https://github.com/JovanLukic79/cali_outdoor_nav/assets/115774118/fddcbc5d-a26d-4074-b853-151a522ddd3c)

## Autonomous Ground Vehicle 

![AGV_2](https://github.com/JovanLukic79/Jovan_Lukic_Portfolio/assets/115774118/44ff29ad-401e-44ec-9323-298e73cc5389)

<ins>Desclaimer:<ins/>
Before getting into the descritption, I would like to iterate that this was my first project working with cross-functioning teams as a junior undergraduate student. The quality of work presented here is not a good representation of what I currently produce. The work that I'm presenting was at a time when I (and many others) were still learning proper design techniques, and gaining intuition in project devlopment. With that said, the main take away of all this is to showcase a certain level of project completion, as well as systems level design in order to have a working platform. This proect was a part of my history, and I intend to showcase my early level work as an engineering student.


This project was intended for the student design completion IGVC. Sarted off by the American Society of Mechanical Engineer (ASME) Student chapter. This project would be in development between October 2019 - January 2021 until focus was shifted elsewhere. During my tenure working on the robotic platform, I started off with assisting in mechanical design of chassis assembly. Being directly involved in multiple design iterations. I verified my designs through the use of hand calculations. This was my first project as an undergrad and it really gave me insight to 'Designing For Manufacturing (DFM)', as well as seeing a design go from conept to product. One of the biggest lessons I learned from this project (aside from DMF), was how vehicle dynamics came into play. One of my earlier iterations had poor mass distribution resulted in the platform losing traction quite easily while turning (However this was later fixed during our re-design). Bellow I will post some of my work, paired with short descriptions.


<ins>Design Iteration I<ins/>

![IGVC_1_Iteration](https://github.com/JovanLukic79/Jovan_Lukic_Portfolio/assets/115774118/690f09d2-3724-4ee3-98cf-b43a1df4ccbb)

- First iteration design concept of a ground robotic platform designed by me and other student engineers

- My addition to this platform was the chassis frame, suspension and drive system

- A modular chassis design made with T-slot extrusions and acrylic sheets as covering were used due to their low cost and manufacturability

- My task was to design chassis frame as well as include all susbsytems, components in the assembly

- I was also tasked with the final editing of the entire assembly before being submitted for a formal design review

<ins>Prototype Demonstration<ins/>

![AGV_1](https://github.com/JovanLukic79/Jovan_Lukic_Portfolio/assets/115774118/11f7f7a2-7c06-4d60-809a-ef3cf60f6cec)

- First iteration of the platform being tested

- Extrusions were cut to length, and was finished off with end-mill

- Brackets were originally purchased but the remainder were manufactured using a water jet cutter on sheet metal 

- Suspension system was ultimately not included due to time constraints (as well as the design was never going to work)

- Redesigned was ultimately needed due to poor mass distribution causing platform to loose traction when turning

<ins>Design Iteration II<ins/>
![IGVC_2_Iteration](https://github.com/JovanLukic79/Jovan_Lukic_Portfolio/assets/115774118/d64f6c33-b63d-4f8c-bfd7-38e2dc6f24e7)

- I was tasked with re-design of the entire platform assembly, this design was compared with other designs in a formal design review
  
- The project development during this project phase was during COVID period meaning we were constrained with parts we already had and machining was not an option resulting in some of the extrusions not being coincident with one another
  
- This design had ideal weight distribution with center mass being low and as close as possible to the drive wheels, resulting in better drive mechanics compare to the first prototype
  
- However design was not chosen due to not meeting weight requirement

<ins>Manufacturing Documents<ins/>

- Technical documents that I've created were used for the second and first iteration robotic platform
  
- Includes bill of materials used second iterative chassis design assembly as well as technical drawing for bracket manufacturing of the first design
  
- Not all documents from this project are included in this gallery
  
<img width="1225" alt="Screen Shot 2023-08-16 at 8 19 44 PM" src="https://github.com/JovanLukic79/Jovan_Lukic_Portfolio/assets/115774118/2a3efe55-015c-4b7a-b78b-5812d2e9375d">

<img width="1227" alt="Screen Shot 2023-08-16 at 8 20 01 PM" src="https://github.com/JovanLukic79/Jovan_Lukic_Portfolio/assets/115774118/d40b7360-7fb6-4946-a9ec-1feaee15cdaf">

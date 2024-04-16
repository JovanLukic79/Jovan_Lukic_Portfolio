# Jovan_Lukic_Portfolio

Hi, My name is Jovan Lukic. I'm currently a volunteer 'Robotics Engineer' at a local startup. My current role revolves around software development of an Unmanned Surface Vehicle (USV) used for oceanic cleanup. I'm creating this portfolio to show off my past work as an undergrad, as well as a professional. I like all things engineering, even though my current focus is in robotics i'm open to any and all industries. While I continue my volunteer work, I am looking for a formal position. With that said, for any future employer who is interested in my past/current work feel free to look over this portfolio. I'm am planning on continuing my learning so as I work on my side project, I will update my portfolio accordingly.

# Scorbot Hardware Interface

Project Link: https://github.com/JovanLukic79/scorbot_control_2

This project is a continuation of 'Project Cali' a mobile manipulator designed by students and staff of California State University Los Angeles (CSULA), and the members of the student organization 'American Society of Mechanical Engineers (ASME). Link: https://github.com/ASME-ground-robot/robot_cali. This platform is intended for reasearch, educational purposes, as well as design competitions. If you would like to read more about the overal project feel free to click on the link provided. I took part in development starting in May 2022, where I acted as a research assistant for a graduate level research, where I worked on developing this controller needed to manipulate the 'Scorbot ER III' robotic arm which was used in development of this platform . I then led further development of 'Project Cali' as a 'Project Lead' from September 2022 - May 2023, where I've done further work in navigation.

![Rover_Urc](https://github.com/JovanLukic79/scorbot_control_2/assets/115774118/f26800ed-8741-468d-a514-e1811fa5fde4)


This repo describes one of my particular contribution of the overall platform which is to provide a control scheme for the 6-link robotic arm integrated onto the overall platform. ROS's 'MoveIt' package was used to provide the control system, and GUI needed for robotic arm manipulation. ROS version that was used is ROS melodic. With that said, this package provides the code needed to interface ros_control and controllers with any sort of embedded controls. Later I may provide an example of said emedded controls just to demonstrate how this package would communicate with a set of hardware controls to acheive joint articulation. For now, I will just provide this part of the system for anyone who needs it as well as to use as my personal portfolio. This package can also be configured to any general robotic arm, so if you happen to need to interface your hardware controls with ROS's control system, feel free to use this as a template. With that said, a description of this package is provided bellow.


![IMG_1666](https://github.com/JovanLukic79/scorbot_control_2/assets/115774118/0d4ebff5-e54c-4485-bf71-09ed5fdbdc6d)

## Description

This repo is made up of two packages. The first one is "scorbot_control_2". This package is where I defined my hardware interface for the robotic arm. In addition to that,"scorbot_control_2" consists of the robotic arm simulation pacakge named "gazebo.launch". The second package is "scorbot_moveit_2", was built using "moveit_setup_assistants". This contains "move_group.launch" the main node needed to communicate with the rest of ROS's control system. In addition to movegroup, this package would also provide moveit_rviz.launch file which woutld act as the main GUI needed to control your robotic arm. 

## Demonstration
![robotic_arm_demo](https://github.com/JovanLukic79/scorbot_control_2/assets/115774118/fde7b4bf-d4aa-48ad-9057-2868b8ec43db)




## Autonomous Ground Vehicle 

![AGV_2](https://github.com/JovanLukic79/Jovan_Lukic_Portfolio/assets/115774118/44ff29ad-401e-44ec-9323-298e73cc5389)

A project intended for the student design completion IGVC. Sarted off by the American Society of Mechanical Engineer (ASME) Student chapter. This project would be in development between October 2019 - January 2021 until focus was shifted elsewhere. During my tenure working on the robotic platform, I started off with assisting in mechanical design of chassis assembly. Being directly involved in multiple design iterations. I verified my designs through the use of hand calculations. This was my first project as an undergrad and it really gave me insight to 'Designing For Manufacturing (DFM)', as well as seeing a design go from conept to product. One of the biggest lessons I learned from this project (aside from DMF), was how vehicle dynamics came into play. One of my earlier iterations had poor mass distribution resulted in the platform losing traction quite easily while turning (However this was later fixed during our re-design). Bellow I will post some of my work, paried with short descriptions.

![IGVC_1_Iteration](https://github.com/JovanLukic79/Jovan_Lukic_Portfolio/assets/115774118/690f09d2-3724-4ee3-98cf-b43a1df4ccbb)

First iteration design concept of a ground robotic platform designed by me and other student engineers

My addition to this platform was the chassis frame, suspension and drive system

A modular chassis design made with T-slot extrusions and acrylic sheets as covering were used due to their low cost and manufacturability

My task was in this iteration was to design a concept for a spring shock absorber fitted with control arms, and power transmission between electric motor and wheel

I was also tasked with the final editing of the entire assembly before being submitted for a formal design review

![AGV_1](https://github.com/JovanLukic79/Jovan_Lukic_Portfolio/assets/115774118/11f7f7a2-7c06-4d60-809a-ef3cf60f6cec)

First iteration of the platform being tested

Extrusions were cut to length, and was finished off with end-mill

Brackets were originally purchased but the remainder were manufactured using a water jet cutter on sheet metal 

Suspension system was ultimately not included due to time constraints

Redesigned due to poor mass distribution causing platform to loose traction when turning


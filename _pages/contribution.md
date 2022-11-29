---
permalink: /contribution/
title: "Contributions"
---

## Software contributions

Our main GitHub repository pointing to every other repository as submodule is available [HERE !](https://github.com/Robocup-Lyontech/robocup-main)

Here are some of the submodules :

- [General Manager](https://github.com/jacques-saraydaryan/robocup_pepper-general_mng)  : we developed a general orchestrator allowing the robot to coordinate its capacities (navigation, perception, interaction) and make decision on defined scenario.

- [Navigation Manager](https://github.com/jacques-saraydaryan/robocup_pepper-navigation_mng) : this functionality provide a set of navigation strategy depending on the observed context. Regarding to the context (lots of people, complex environment, large free space zone), the robot changes it way of navigation.


- [People Manager](https://github.com/Robocup-Lyontech/People-Management-Framework) : We developed a framework that allows the extraction of high-level person features from a 2D camera in addition to tracking people over time. The proposed people management framework aggregates body and person features including an original pose estimation using only a 2D camera. At this time, people pose and posture, clothing colors, face recognition are combined with tracking and re-identification abilities.
  
<img src="/assets/images/contribution/people_mng_exp.png" width="700" ALIGN="middle" >

This framework includes the following additional contributions:
  - [Face recognition](https://github.com/jacques-saraydaryan/ros_face_recognition) : a solution was developed to automatically catch face and learn it for future detection.
  - [Color detection](https://github.com/jacques-saraydaryan/ros_color_detection) : we extract main colors of a given picture (e.g t-shir, trousers) based on HSV format and K-mean clustering 
  - [Pose detection](https://github.com/m0rph03nix/ros_openpose_gossip) : based on the OpenPose data, we build a pose extractor gives us the estimate pose (stand, sit, lying down, left or right arm up,...) and distance estimation

## Previous results and works around RoboCup
**LyonTech** is composed by former members of CPE Lyon team and by former candidates for Robocup organization:
- **LyonTech**  team : **2nd place at Robocup@home SSPL** OnLine, World **2021**
- **LyonTech**  team : **6th place at Robocup@home OPL** OnLine, World **2021**
- **LyonTech**  team : **3rd place at Robocup@home SSPL** Sydney, AUSTRALIA, **2019**
- **LyonTech** team : **5th place at Robocup@home SSPL** Montreal, CANADA, **2018**
- **CPE Robot Forum** team (including Jacques Saraydaryan, Raphael Leber, Fabrice Jumel) : **15th place at Robocup@home OPL** Leipzig, Germany, **2016**
- **Lyon CPE** team  (including Jacques Saraydaryan, Fabrice Jumel): **3rd place at Robocup@work**, Joao Pessoa, Brazil, **2013**


- Lyon city and INSA **candidated for the organization of the Robocup, in 2016** (co-led by Olivier Simonin from Chroma/CITI team).
- Fabrice Jumel (CPE Lyon/CITI) is a **Robocup@home evangelist** for France
  - He is  OC member of RoboCup@Home since 2017.    
  - He was OC chair and co-chair in 2018-2020 and  TC of RoboCup@Home in 2017-2018
  - He is member as the organisation commitee for application of Bordeaux for **Robocup 2020** 
  - He was  the Organizer of a French @home open (first edition 24, 25th January 2018 in Lyon). 
  - He was **OC for Robocup@home SSPL in Nagoya and Montreal** and **OC for Robocup@home LARC in Recife**.


## Contributions at the robocup Symposium :
- [People management framework using a 2D camera for human-robot social interactions](https://hal.archives-ouvertes.fr/hal-02318916), **Best scientific paper**, **2019** 
- [Towards S-NAMO: Socially-aware Navigation Among Movable Obstacles](https://hal.archives-ouvertes.fr/hal-02293242/file/Towards_Social_NAMO.pdf), **2019**
- [Context Aware Robot Architecture, Application to the RoboCup@Home Challenge](https://hal.archives-ouvertes.fr/hal-01832613/file/context-aware-robot-revised.pdf), **2018**	

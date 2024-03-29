---
permalink: /sspl/
title: "Social Standard Plateform League"
---
<iframe width="560" height="315" src="https://www.youtube.com/embed/6DnTP3k-580" frameborder="0" allowfullscreen></iframe>

In the case of SSPL league, the standard plateform is a pepper robot from Softbanks robotics. We are not allowed to modify the robot but we could use some external computing devices.
<img src="/assets/images/sspl/pepper_iron.PNG" width="700" ALIGN="middle" >

The architecture of **LyonTech**'s embedded AI software is shown below [17] :

<img src="/assets/images/archi.png" width="700" ALIGN="middle" >

It contains modules which have been developed in different research groups of the consortium, completed by ofthe shelf modules which tackle standard tasks, as well as engineering bricks interconnecting these modules.




## Perception
Our computer vision experts bring knowledge in 
- gesture recognition [1], 
- activity recognition [2, 3]
- articulated pose estimation [4], 
- semantic segmentation [5]
- object recognition [6]. 

A large part of these methods are capable of running on real time and have been integrated in our platforms of mobile robots. Our combined work allows us to be aware of the objects present in a room, their locations, as well as the ongoing activities in this room.


## Motion planning and Decision making
Our expertise in robotics relates to motion planning in dynamic and uncertain environments, mapping, localization and decision-making for single and multi-robot systems. The work focuses on autonomous navigation in crowded environments (human-aware navigation) and in urban traffic (autonomous vehicles) for human assistance [7,9]. We also explore robot and  cooperation for human scene observation [10], 3D environment mapping, transport and service delivery [11]. We experiment and evaluate the models with Pepper humanoids, fleets of mobile robots (cf. Figure 2) and UAVs, and two equipped/autonomous cars (see https://team.inria.fr/chroma/en/plate-formes/). 

## Human-Robot Interactions 
We have been working for years on different interactions with robots (from teleoperation to multirobots orchestration [12,15]). Since this year, we also get strong support from the Hoomano company, which creates solutions for Human-Robot interaction in real world applications, in particular for Pepper robots.

## Integration 
All components are integrated using the ROS middleware, which is the base system of our robot. ROS offers the ability to connect a set of programs through synchronous and asynchronous communication. Moreover, by allowing a set of heterogeneous components (probes, actuators, services) to communicate in a normalized way, processing program can be reused. The **naoqi sdk**, provided by **softbank/aldebaran** with the **Pepper robot**, gives a set of API that is mainly used for Robot and Human interactions (speech recognition, text to speech, robot behavior feedbacks). In order to highlight the robot activity, the Pepper tablet gives visual feedbacks (javascript framework).

We define five principal functionality blocks in our architecture:
The **Robot Navigation Manager** is in charge of localizing the robot and allowing dynamic navigation (obstacles avoidance). The analysis of the robot  environment is performed by **Object Detection** and recognition modules, mainly deep neural networks developed inhouse [6] or of-the-shelf modules like YOLO 9000 [16]. Labeled object positions are provided to other blocks.

All human robot interactions are managed by the **Robot Human interaction** block embedded in the robot. The robot also maintains a knowledge database about its environment with the **world mapping** unit(humans, objects and points of interest positions).

Finally, the **general manager block** works like an orchestrator and gives order to other blocks in order to achieve scenarios.


## References 

1. N. Neverova, C. Wolf, G.W. Taylor, and F. Nebout. [Moddrop: adaptive multimodal gesture recognition.](https://arxiv.org/pdf/1501.00102.pdf) IEEE Transactions on Pattern Analysis and Machine Intelligence (PAMI), 2016.
2. F. Baradel, C. Wolf, and J. Mille. [Human action recognition: Pose-based attention draws focus to hands.](http://liris.cnrs.fr/christian.wolf/papers/iccv2017ws.pdf) In ICCV Workshop on Hands in Action, 2017.
3. F. Baradel, C. Wolf, and J. Mille. [Pose-conditioned spatio-temporal attention for human action recognition](https://arxiv.org/pdf/1703.10106.pdf). Pre-print: arxiv:1703.10106, 2017.
4. N. Neverova, C. Wolf, G.W. Taylor, and F. Nebout. [Hand pose estimation through weakly-supervised learning of a rich intermediate representation](https://arxiv.org/pdf/1511.06728.pdf). To appear in Computer Vision and Image Understanding (CVIU), 2017.
5. D. Fourure, R. Emonet, E. Fromont, D. Muselet, A. Trémeau, and C. Wolf. [Residual conv-deconv grid network for semantic segmentation.](https://arxiv.org/pdf/1707.07958.pdf) In British Machine Vision Conference (BMVC), 2017.
6. B. Moysset, J. Louradour, and C. Wolf. [Learning to detect and localize many objects from few examples](https://arxiv.org/pdf/1611.05664.pdf). Pre-print: arxiv:1611.05664, 2016.
7. F. Jumel, J. Saraydaryan, and O. Simonin. Mapping likelihood of encountering humans: application to path planning in crowded environment. In The Euro pean Conference on Mobile Robotics (ECMR), Proceedings of ECMR 2017, Paris, France, September 2017.
8. M. Barbier, C. Laugier, O. Simonin, and J. Ibanez-Guzman. Classication of Drivers Manoeuvre for Road Intersection Crossing with Synthetic and Real Data.
In 2017 IEEE Intelligent Vehicles Symposium (IV), Los Angeles, United States, June 2017.
9. M. Andries, O. Simonin, and F. Charpillet. [Localisation of humans, objects and robots interacting on load-sensing 
floors.](https://hal.inria.fr/hal-01196042v2/document) IEEE Sensors Journal, PP(99):12, 2015.
10. L. Matignon, S. D'Alu, and O. Simonin. [Multi-robot human scene observation based on hybrid metric-topological mapping.](https://ojs.cvut.cz/ojs/index.php/ap/article/view/AP.2015.55.0169) In European Conference on Mobile Robotics (ECMR), 2017.
11. J. Saraydaryan, F. Jumel, and O. Simonin. Robots delivering services to moving people : Individual vs. group patrolling strategies. In IEEE ARSO, 2015.
12. A. Gréea, J. Saraydaryan, F. Jumel, and A. Guenard. [A robotic and automation services ontology, architectures logicielles pour la robotique autonome, les systemes  cyber-physiques et les systémes auto-adaptables.](https://antoine.grea.me/astro/) In CAR, 2015.
13. L. Sevrin, N. Noury, N. Abouchi, F. Jumel, B. Massot, and J. Saraydaryan. Preliminary results on algorithms for multi-kinect trajectory fusion in a living lab. In IRBM, 2015.
14. J. Saraydaryan, F. Jumel, and Adrien Guenard. [Astro: Architecture of services toward robotic objects.](https://www.ijcsi.org/papers/IJCSI-11-4-1-1-9.pdf) In IJCSI, 2014.
15. E.Nauer A. Cordier, E. Gaillard. Man-machine collaboration to acquire adaptation knowledge for a case-based reasoning system. In ACM DL, editor, WWW 2012 { SWCS'12 Workshop, pages 1113{1120, Lyon, France, April 2012. ACM.
16. J. Redmon and A. Farhadi. Yolo9000: Better, faster, stronger. In CVPR, 2017.
17. F. Jumel, J. Saraydaryan, R. Leber, L. Matignon, E. Lombardi, C. Wolf, and O. Simonin. Context Aware Robot Architecture,
Application to the RoboCup@Home Challenge. In RoboCup symposium, Montreal, Canada, June 2018.
18. F. Jumel, J. Saraydaryan, and O. Simonin. Mapping likelihood of encountering humans: application to path planning in crowded environment. In The European Conference on Mobile Robotics (ECMR), Proceedings of ECMR 2017, Paris, France, September 2017.
17. F. Jumel, J. Saraydaryan, R. Leber, L. Matignon, E. Lombardi, C. Wolf, and O. Simonin. Context Aware Robot Architecture,
Application to the RoboCup@Home Challenge. In RoboCup symposium, Montreal, Canada, June 2018.
18. F. Jumel, J. Saraydaryan, and O. Simonin. Mapping likelihood of encountering humans: application to path planning in crowded environment. In The European Conference on Mobile Robotics (ECMR), Proceedings of ECMR 2017, Paris, France, September 2017.
19.  F. Jumel.  Advancing research at the robocup@home competition . IEEE Robotics Automation Magazine, 26(2):7–9, 2019
20.  J. Saraydaryan, R. Leberl, and F. Jumel.  People managementframework using a 2D camera for human-robot social interactions. In23rd AnnualRoboCup International Symposium RCS, Sydney, Australia, July 2019
21.  O. Simonin, B. Renault B., J. Saraydaryan Modeling a social placement cost to extendnavigation  among  movable  obstacles  (namo)  algorithms.  IEEE/IROS,2020.




---
permalink: /approach/
title: "Scientific approach for Robocup@home"
---


The architecture of **LyonTech**'s embedded AI software is shown in Figure 3. It contains modules which have been developed in different research groups of the consortium, completed by ofthe shelf modules which tackle standard tasks, as well as engineering bricks interconnecting these modules. 
**The scientic expertise of the consortium** is broad and targets the needs of the competition:

<object  width="100%" data="https://youtu.be/TPTh_KjVUJQ">  </object>


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

1. N. Neverova, C. Wolf, G.W. Taylor, and F. Nebout. Moddrop: adaptive multimodal gesture recognition. IEEE Transactions on Pattern Analysis and Machine Intelligence (PAMI), 2016.
2. F. Baradel, C. Wolf, and J. Mille. Human action recognition: Pose-based attention draws focus to hands. In ICCV Workshop on Hands in Action, 2017.
3. F. Baradel, C. Wolf, and J. Mille. Pose-conditioned spatio-temporal attention for human action recognition. Pre-print: arxiv:1703.10106, 2017.
4. N. Neverova, C. Wolf, G.W. Taylor, and F. Nebout. Hand pose estimation through weakly-supervised learning of a rich intermediate representation. To appear in Computer Vision and Image Understanding (CVIU), 2017.
5. D. Fourure, R. Emonet, E. Fromont, D. Muselet, A. Trémeau, and C. Wolf. Residual conv-deconv grid network for semantic segmentation. In British Machine Vision Conference (BMVC), 2017.
6. B. Moysset, J. Louradour, and C. Wolf. Learning to detect and localize many objects from few examples. Pre-print: arxiv:1611.05664, 2016.
7. F. Jumel, J. Saraydaryan, and O. Simonin. Mapping likelihood of encountering humans: application to path planning in crowded environment. In The Euro pean Conference on Mobile Robotics (ECMR), Proceedings of ECMR 2017, Paris, France, September 2017.
8. M. Barbier, C. Laugier, O. Simonin, and J. Ibanez-Guzman. Classication of Drivers Manoeuvre for Road Intersection Crossing with Synthetic and Real Data.
In 2017 IEEE Intelligent Vehicles Symposium (IV), Los Angeles, United States, June 2017.
9. M. Andries, O. Simonin, and F. Charpillet. Localisation of humans, objects and robots interacting on load-sensing 
oors. IEEE Sensors Journal, PP(99):12, 2015.
10. L. Matignon, S. D'Alu, and O. Simonin. Multi-robot human scene observation based on hybrid metric-topological mapping. In European Conference on Mobile Robotics (ECMR), 2017.
11. J. Saraydaryan, F. Jumel, and O. Simonin. Robots delivering services to moving people : Individual vs. group patrolling strategies. In IEEE ARSO, 2015.
12. A. Gréea, J. Saraydaryan, F. Jumel, and A. Guenard. A robotic and automation services ontology, architectures logicielles pour la robotique autonome, les systemes  cyber-physiques et les systémes auto-adaptables. In CAR, 2015.
13. L. Sevrin, N. Noury, N. Abouchi, F. Jumel, B. Massot, and J. Saraydaryan. Preliminary results on algorithms for multi-kinect trajectory fusion in a living lab. In IRBM, 2015.
14. J. Saraydaryan, F. Jumel, and Adrien Guenard. Astro: Architecture of services toward robotic objects. In IJCSI, 2014.
15. E.Nauer A. Cordier, E. Gaillard. Man-machine collaboration to acquire adaptation knowledge for a case-based reasoning system. In ACM DL, editor, WWW 2012 { SWCS'12 Workshop, pages 1113{1120, Lyon, France, April 2012. ACM.
16. J. Redmon and A. Farhadi. Yolo9000: Better, faster, stronger. In CVPR, 2017.



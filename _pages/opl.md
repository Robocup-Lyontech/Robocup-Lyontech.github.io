---
permalink: /opl/
title: "Open Plateform League"
---

<!-- <iframe width="560" height="315" src="https://www.youtube.com/embed/am0lZ7B3gYM" frameborder="0" allowfullscreen></iframe> -->

<img src="/assets/images/opl/OPLPlateformev3t.png" ALIGN="right" width="180" >

Our Open Platform named **Palbator** is made from a PMB-2 PAL mobile base, enhanced by several hardware and software features. It's body contains a 7 DoF (1P + 6R) custom arm made of 1 prismatic joint (elevator) and 6 revolute joints. It's designed to reach objects on the floor or on a top shelf (~1m80) with a 1.5Kg payload.

<img src="/assets/images/opl/robot_archi_hard_OPL2023_V1.png" width="480" ALIGN="center" >  


Our software architecture is distributed on several hardware platforms as shown below. As we use ROS and independent software modules, we can easily (un)scale our hardware .

<img src="/assets/images/opl/archi_hard_soft.png" width="600" ALIGN="middle" >

The architecture of LyonTech's software is shown below. It contains modules which have been developed in the different research groups of the consortium, completed by off-the shelf modules which tackle standard tasks, as well as engineering bricks interconnecting these modules.

<img src="/assets/images/opl/architecture2020_v2_OPL.png" width="600" ALIGN="middle" >


**The scientic expertise of the consortium** is broad and targets the needs of the competition:

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


## Human-Robot Interaction
Human-Robot Interaction is managed with a classical combination of natural language communication and use of a tablet.

 For Natural Language Understanding (NLU), we are using the off-the-shelf solution, free for non-commercial use software Snips. Snips offer a way to construct an offline solution for speech recognition. 
Snips uses very few resources that it can be embedded on a Raspberry Pi. We use an array of microphones (matrix creator one)  to improve sound localization .

Concerning text-to-speech, we are using the classical open source solution Espeak, another solution Acapella is being explored. 

 For tablet interaction, we reused a web application (based on ReactJS) developed for  pepper robot  and successfully used during SSPL robocup@home competition in Sydney. 


## Integration 
The Ros Middleware is used to integrate components (customized packages and LyonTech packages), set of functional blocks are orchestrated through a General manager. 

Our robot evolves in an [apartment-like arena](https://robocup-lyontech.github.io/bordeaux/The-Robotic-Arena/)

We are still in the process of customizing the robot to fit the robocup environnement : [Exemple with a hack of the PAL base](https://robocup-lyontech.github.io/bordeaux/The-baby-cup-case/)



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



---
title: "The \"baby cup\" case"
categories:
  - Bordeaux
tags:
  - robocup
---
9 cm: that is the height of the laser scan of the lidar on the robot base.</br>
6 cm: that is the height of a cup of tea.</br>
When you said that, you said everything.

If we did not want that the robot spill a coffee cup landing on the ground and wastes this precious amount of energy, we had to add new sensors in order to prevent such a tragic event. So that is what we did !

A miro-controler, some ToF sensor, a couple of welding later and we created a system capable of detecting low obstacles such as a coffe cup, but also the tip of a foot that the 50kg robot can step on if not detected.

For the sensors, we used VL53L0X sensor because they are simple to use, efficient and space-saving. We put 3 of them so that we cover a cone in the front of the robot which is the most important because it only go forward. They use I²C protocol wich is really easy to set up with common micro-controlers.

We used for that an Arduino MEGA with the ros libraries (microcontroler and computer) to pass our ros environment the sensor informations. An Arduino MEGA was nécessary for memory purposes (ROS librairy and VL53L0X object are quite important).

This is what the V0 looked like:

![ToF_v0](/assets/images/articles/tof_v0.jpg)

So we had ranges that tell where the baby cup is and in wich direction, published in a ros message one after the other. The problem is that the ros local_costmap layer only take LaserScan or PointCloud. So we tranform this range topic into a Laserscan topic so that we can integrate it into the Ros Navigation Stack. The 3 range sensor are seen by the robot as an lidar in the middle of the robot who take 3 measurements on a restricted angle, like that:

![simulated_lidar_schematic](/assets/images/articles/simulated_lidar.png)

As the Tof are not exactly linear, according to the datasheet, we calculate the angle that allows us not to detect ground as an obstacle and reduces the dead zone near the sensor.

![sensor_mount_schematic](/assets/images/articles/tof_mount.png)

To do so, we model and 3D print support to attach the sensor correctly to the base at the correct angle. At the begining, we glue the suport to the base in order proof the position and see the real result.

![hot_glue_picture](/assets/images/articles/hot_glue.jpg)

In order to create something removable and upgradable, we create a shield for the arduino MEGA.

![arduino_shield](/assets/images/articles/arduino_shield.jpg)

And then we finish the implementation of the new functionality into the robot.

![result_picture](/assets/images/articles/result.jpg)

Baby cup problem? **Deal with it!**

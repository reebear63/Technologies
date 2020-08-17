# ROS is not an Operating System #

Although ROS is short for "Robot Operating System", ROS is not an operating system. 
https://en.wikipedia.org/wiki/Robot_Operating_System

Robot Operating System (ROS or ros) is a robotics middleware (i.e. a collection of software frameworks for robot software development).

Although ROS is not an operating system, it provides services designed for a heterogeneous computer cluster such as hardware abstraction, low-level device control, implementation of commonly used functionality, message-passing between processes, and package management. Running sets of ROS-based processes are represented in a graph architecture where processing takes place in nodes that may receive, post and multiplex sensor data, control, state, planning, actuator, and other messages. Despite the importance of reactivity and low latency in robot control, ROS itself is not a real-time OS (RTOS). It is possible, however, to integrate ROS with real-time code. The lack of support for real-time systems has been addressed in the creation of ROS 2.0, a major revision of the ROS API which will take advantage of modern libraries and technologies for core ROS functionality and add support for real-time code and embedded hardware.

Software in the ROS Ecosystem can be separated into three groups:
* language- and platform-independent tools used for building and distributing ROS-based software;
* ROS client library implementations such as roscpp, rospy, and roslisp;
* packages containing application-related code which uses one or more ROS client libraries.
  
Both the language-independent tools and the main client libraries (C++, Python, and Lisp) are released under the terms of the BSD license, and as such are open source software and free for both commercial and research use. The majority of other packages are licensed under a variety of open source licenses. These other packages implement commonly used functionality and applications such as hardware drivers, robot models, datatypes, planning, perception, simultaneous localization and mapping, simulation tools, and other algorithms.

The main ROS client libraries are geared toward a Unix-like system, primarily because of their dependence on large collections of open-source software dependencies. For these client libraries, Ubuntu Linux is listed as "Supported" while other variants such as Fedora Linux, macOS, and Microsoft Windows are designated "experimental" and are supported by the community. The native Java ROS client library, rosjava, however, does not share these limitations and has enabled ROS-based software to be written for the Android OS. rosjava has also enabled ROS to be integrated into an officially supported MATLAB toolbox which can be used on Linux, macOS, and Microsoft Windows. A JavaScript client library, roslibjs has also been developed which enables integration of software into a ROS system via any standards-compliant web browser.

## History ##

1. **Early days at Stanford (2007 and earlier)**
Sometime before 2007, the first pieces of what eventually would become ROS were beginning to come together at Stanford University. Eric Berger and Keenan Wyrobek, PhD students working in Kenneth Sailsbury's robotics laboratory at Stanford, were leading the Personal Robotics Program. While working on robots to do manipulation tasks in human environments, the two students noticed that many of their colleagues were held back by the diverse nature of robotics: an excellent software developer might not have the hardware knowledge required, someone developing state of the art path planning might not know how to do the computer vision required. In an attempt to remedy this situation, the two students set out to make a baseline system that would provide a starting place for others in academia to build upon. In the words of Eric Berger, “something that didn’t suck, in all of those different dimensions”.

In their first steps towards this unifying system, the two build the PR1 as a hardware prototype and began to work on software from it, borrowing the best practices from other early open source robotic software frameworks, particularly switchyard, a system that Morgan Quigley, another Stanford PhD student, had been working on in support of the STAIR (STanford Artificial Intelligence Robot) by the Stanford Artificial Intelligence Laboratory.  Early funding of US$50,000 was provided by Joanna Hoffman and Alain Rossmann, which supported the development of the PR1. While seeking funding for further development, Eric Berger and Keenan Wyrobek met Scott Hassan, the founder of Willow Garage, a technology incubator which was working on an autonomous SUV and a solar autonomous boat.  Hassan shared Berger and Wyrobek's vision of a “Linux for robotics”, and invited them to come and work at Willow Garage.  Willow Garage was started in January 2007, and the first commit of ROS code was made to SourceForge on the seventh of November, 2007.

2. **Willow Garage (2007-2013)**
Willow Garage began developing the PR2 robot as a follow-up to the PR1, and ROS as the software to run it. Groups from more than twenty institutions made contributions to ROS, both the core software and the growing number of packages which worked with ROS to form a greater software ecosystem. The fact that people outside of Willow were contributing to ROS (particularly from Stanford's STAIR project) meant that ROS was a multi-robot platform from the beginning. While Willow Garage had originally had other projects in progress, they were scrapped in favor of the Personal Robotics Program: focused on producing the PR2 as a research platform for academia and ROS as the open source robotics stack that would underlie both academic research and tech startups, much like the LAMP stack did for web-based startups.

In December 2008, Willow Garage met the first of their three internal milestones: continuous navigation for the PR2 over a period of two days and a distance of pi kilometers. Soon after, an early version of ROS (0.4 Mango Tango) was released, followed by the first RVIZ documentation and the first paper on ROS. In early summer, the second internal milestone: having the PR2 navigate the office, open doors, and plug itself it in, was reached. This was followed in August by the initiation of the ROS.org website. Early tutorials on ROS were posted in December, preparing for the release of ROS 1.0, in January 2010. This was Milestone 3: producing tons of documentation and tutorials for the enormous capabilities that Willow Garage's engineers had developed over the preceding 3 years.

The first official ROS distribution release: ROS Box Turtle, was released on March 2 of 2010, marking the first time that ROS was official distributed with a set of versioned packages for public use. These developments lead to the first drone running ROS, the first autonomous car running ROS, and the adaption of ROS for Lego Mindstorms. With the PR2 Beta program well underway, the PR2 robot was officially released for commercial purchase on September 9, 2010.

Willow Garage began 2012 by creating the Open Source Robotics Foundation (OSRF) in April. The OSRF was immediately awarded a software contract by DARPA. Later that year, the first ROSCon was held in St. Paul, MN, the first book on ROS, ROS By Example, was published, and the Baxter, first commercial robot to run ROS, was announced by Rethink Robotics. Soon after passing its fifth anniversary in November, ROS began running on every continent on December 3, 2012.

In February 2013, the OSRF became the primary software maintainers for ROS, foreshadowing the announcement in August that Willow Garage would be absorbed by its founders, Suitable Technologies. At this point, ROS had released seven major versions (up to ROS Groovy), and had users all over the globe.  This chapter of ROS development would be finalized when Clearpath Robotics took over support responsibilities for the PR2 in early 2014.

3. **OSRF and Open Robotics (2013-present)**
In the years since OSRF took over primary development of ROS, a new version has been released every year, while interest in ROS continues to grow. ROSCons have occurred every year since 2012, co-located with either ICRA or IROS, two flagship robotics conferences. Meetups of ROS developers have been organized in a variety of countries, a number of ROS books have been published, and many educational programs initiated. On September 1, 2014, NASA announced the first robot to run ROS in space: Robotnaut 2, on the International Space Station. In 2017, the OSRF changed its name to Open Robotics.  Tech giants Amazon and Microsoft began to take an interest in ROS during this time, with Microsoft porting core ROS to Windows in September 2018, followed by Amazon Web Services releasing RoboMaker in November.

Perhaps the most important development of the OSRF/Open Robotics years thus far (not to discount the explosion of robot platforms which began to support ROS or the enormous improvements in each ROS version) was the proposal of ROS2, a significant API change to ROS which is intended to support real time programming, a wider variety of computing environments, and utilize more modern technology. ROS2 was announced at ROSCon 2014, the first commits to the ros2 repository were made in February 2015, followed by alpha releases in August 2015. The first distribution release of ROS2, Ardent Apalone, was released on December 8, 2017, ushering in a new era of next-generation ROS development.

## Tools ##
ROS's core functionality is augmented by a variety of tools which allow developers to visualize and record data, easily navigate the ROS package structures, and create scripts automating complex configuration and setup processes. The addition of these tools greatly increases the capabilities of systems using ROS by simplifying and providing solutions to a number of common robotics development. These tools are provided in packages like any other algorithm, but rather than providing implementations of hardware drivers or algorithms for various robotic tasks, these packages provide task and robot-agnostic tools which come with the core of most modern ROS installations.

1. rviz
rviz is a three-dimensional visualizer used to visualize robots, the environments they work in, and sensor data. It is a highly configurable tool, with many different types of visualizations and plugins.

2. rosbag
rosbag is a command line tool used to record and playback ROS message data. rosbag uses a file format called bags, which log ROS messages by listening to topics and recording messages as they come in. Playing messages back from a bag is largely the same as having the original nodes which produced the data in the ROS computation graph, making bags a useful tool for recording data to be used in later development. While rosbag is a command line only tool, rqt_bag provides a GUI interface to rosbag.

3. catkin
catkin is the ROS build system, having replaced rosbuild as of ROS Groovy. catkin is based on CMake, and is similarly cross-platform, open source, and language-independent.

4. rosbash
The rosbash package provides a suite of tools which augment the functionality of the bash shell. These tools include rosls, roscd, and roscp, which replicate the functionalities of ls, cd, and cp respectively. The ROS versions of these tools allow users to use ros package names in place of the filepath where the package is located. The package also adds tab-completion to most ROS utilities, and includes rosed, which edits a given file with the chosen default text editor, as well rosrun, which runs executables in ROS packages. rosbash supports the same functionalities for zsh and tcsh, to a lesser extent.

5. roslaunch
roslaunch is a tool used to launch multiple ROS nodes both locally and remotely, as well as setting parameters on the ROS parameter server. roslaunch configuration files, which are written using XML can easily automate a complex startup and configuration process into a single command. roslaunch scripts can include other roslaunch scripts, launch nodes on specific machines, and even restart processes which die during execution.

## Gazebo simulator ##
Gazebo is an open-source 3D robotics simulator. Gazebo was a component in the Player Project from 2004 through 2011. Gazebo integrated the ODE physics engine, OpenGL rendering, and support code for sensor simulation and actuator control. In 2011, Gazebo became an independent project supported by Willow Garage. In 2012, Open Source Robotics Foundation (OSRF) became the steward of the Gazebo project. OSRF changed its name to Open Robotics in 2018.

Gazebo can use multiple high-performance physics engines, such as ODE, Bullet, etc (the default is ODE). It provides realistic rendering of environments including high-quality lighting, shadows, and textures. It can model sensors that "see" the simulated environment, such as laser range finders, cameras (including wide-angle), Kinect style sensors, etc.

http://gazebosim.org/

Robot simulation is an essential tool in every roboticist's toolbox. A well-designed simulator makes it possible to rapidly test algorithms, design robots, perform regression testing, and train AI system using realistic scenarios. Gazebo offers the ability to accurately and efficiently simulate populations of robots in complex indoor and outdoor environments. At your fingertips is a robust physics engine, high-quality graphics, and convenient programmatic and graphical interfaces. Best of all, Gazebo is free with a vibrant community.


## ROS versions and releases ##
ROS releases may be incompatible with other releases and are often referred to by code name rather than version number. ROS currently releases a version every year in May, following the release of Ubuntu LTS versions. ROS2 currently releases a new version every six months (in December and July). These releases are supported for a single year.

# Robotics and the Raspberry Pi #

## ROSberryPi / Installing ROS Kinetic on the Raspberry Pi ##
http://wiki.ros.org/ROSberryPi/Installing%20ROS%20Kinetic%20on%20the%20Raspberry%20Pi

Description: 
This instruction covers the installation of ROS Kinetic on the Raspberry Pi 2, 3, or 4 with Raspbian Jessie, Stretch, or Buster. However as final repositories are available now, today it is faster and easier to use Ubuntu Mate 16.04 (Xenial, download here) together with the standard ARM installation instructions here. An SD Card Image with Ubuntu 16.04 (LXDE) and ROS Kinetic installed can be downloaded here for the Raspberry Pi 3.

## GoPiGo3 ##
Dexter Industries (dexterindustries.com)

buy at:
- RobotShop.com -- Mirabel, Quebec, Canada
- Génération Robots -- generationrobots.com -- Bordeaux, Filiale in Berlin
- ThePiHut, Suffolk, England
  
* GoPiGo3 base kit (about 100 EUR)
  * GoPiGo board
  * chassis, wheels, motors, encoders, power battery pack
  
* GoPiGo3 starter kit (about 220 EUR)
  * Raspberry Pi 3, mini WiFi dongle
  * GoPiGo server package, distance sensor, microSD card (with DexterOS software)
  * 8 GB USB drive
  * power supply

https://gopigo3.readthedocs.io/en/master/

Einkaufsliste
--------------
- GoPiGo3 base kit (101,15)
- RasPi Kamera v2  ( 29,90)
- Laserscanner     ( 23,95) = Distance Sensor
- IMU Sensor (Inertial Measurement Unit, Accelerometer, Gyroscope, Compass Sensor)
- 

## Zusammenbau des GoPiGo3 ##
https://edu.workbencheducation.com/cwists/preview/26659-build-your-gopigo3-stage-1x
https://gopigo3.readthedocs.io/en/master/

## Programming GoPiGo3 ##
https://gopigo3.readthedocs.io/en/master/tutorials-basic/driving.html


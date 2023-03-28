# Choreographing Movement
Arushi Nigam (an452), Antony Tahan (at674), Celine Lee (cl923)

It is about time to have a functioning mobile robot! Starting from this lab, you should prioritize either robot building and/or study design. 

## Prep
### Watch the following tutorials:
- [How to crimp wires](https://www.youtube.com/watch?v=SaU00MMjzn0&ab_channel=GrizzlyBuilds)

- [Beginner's Guide on Soldering](https://www.makerspaces.com/how-to-solder/)


- [How to Solder Wires Together](https://youtu.be/NSqPHQ1zQco)



### For this lab, you will need:
1. Your laptop
2. Cardboard
3. Utility knife
4. Your hoverboard base

### Deliverables for this lab are: 

0. Photos of your robot prototype
1. A video of your robot moving around
2. A sketch of a series movements based on your final project
3. A video showing your robot perform the movements in item #2.
4. Reflect upon your design, what would you do differently?


## Lab Overview
For this assignment, you are going to:

A) [Build your chassis](#part-a-build-your-chassis)

B) [Move it around](#part-b-move-it-around)

C) [Plan a movement](#part-c-plan-a-movement)

D) [Optional Spinning your LiDAR](#part-d-optional-spinning-your-LiDAR)

Labs are due on Tuesdays before class. Make sure this page is linked to on your main class hub page.

## Part A. Build your chassis
If you haven't already, now is a good time to actually mockup a low fidelity version robot for your final project. At least, you should have a chassis that safely host all the hardware you have (ODrive, wheels, battery, etc).

Feel free to use any material we have in lab to build your chassis. Things you might find useful are cardboard, gluegun, zip ties, duo locks, etc. 

## Part B. Move it around
Once you build your chassis, test it out! Power on your hoverboard and connect your controller. Drive your robot around! (Take a video while you do that!)

A few questions to consider:
- when your robot accelerate, is the chassis stable?
- what are all the possible motions (action space) your robot can perform? (e.g. rotating in place, moving foward/backward, ...)
- reflect on your design and think what would you do differently next time.

## Part C. Plan a movement
Based on your scenario, sketch out a sequence of movement in a storyboard format. 
Then, control your robot to execute that sequence of movement. (Take a video while you do that!)


## Part D. Optional spinning your LiDAR
If you plan to use LiDAR for your final project, or are simply curious about how it works, let's set it up!

```
# Install LiDAR SDK
# In your RPi terminal
sudo apt install cmake pkg-config
cd ~
git clone https://github.com/YDLIDAR/YDLidar-SDK.git
cd YDLidar-SDK
mkdir build
cd build
cmake ..
make
sudo make install
```

```
cd ~/mobilehri_ws/src/mobilehri2023
git checkout ydlidar_ros2_driver
cd ~/mobilehri_ws
colcon build

chmod 0777 src/ydlidar_ros2_driver/startup/*
sudo sh src/ydlidar_ros2_driver/startup/initenv.sh

```
Now, plug in your LiDAR.
```
# start your LiDAR
source install setup.bash
ros2 launch ydlidar_ros2_driver ydlidar_launch.py 
```

To visualize your LiDAR reading, open foxglove studio in vnc viewer. Then, click 3D in the left panel.

### Again, deliverables for this lab are: 

0. Photos of your robot prototype 
<img width="457" alt="Screen Shot 2023-03-28 at 10 39 37 AM" src="https://user-images.githubusercontent.com/31280357/228274969-032ac15b-2629-4127-863d-41a4a85c9940.png">

<img width="291" alt="Screen Shot 2023-03-28 at 10 40 53 AM" src="https://user-images.githubusercontent.com/31280357/228275371-6c2d9d35-fd9b-4a0c-81f1-ea7623aba3a0.png">
1. A video of your robot moving around
    TBD
2. A sketch of a series movements based on your final project
<img width="734" alt="Screen Shot 2023-03-28 at 10 41 17 AM" src="https://user-images.githubusercontent.com/31280357/228275495-961a089d-786c-44f9-975a-5480e0ca95d3.png">
3. A video showing your robot perform the movements in 2.
  TBD

4. Reflect upon your design, what would you do differently?
I think we took a lot of time in trying to figure out the mechanics for the robot. For example, just carving out a perfect shape for the wheels to fit took us one entire lab.
I would definitely plan better and delegate different activities so that we effectively utilize time. 



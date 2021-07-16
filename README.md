# Using SLAM map to launch the navigation

Navigation Simulation

Before we start, we need to do the previous task to get the map.

to see the previous task, click on this link: https://github.com/Mahaalt/Using-Turtlebot3-with-SLAM-approach 

First, we need to close all the Terminal windows and open a new one, then write this command to open the TurtleBot3 world:

`$ roslaunch turtlebot3_gazebo turtlebot3_world.launch`

---

Second, we will run the navigation node by writing this command in a new Terminal window:

`$ roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/map.yaml`

Note: if your home destination has another name, please change the word HOME to your one.

![01](https://user-images.githubusercontent.com/71232960/125881090-a552b472-fdca-4253-a8da-fdadfbf02c73.png)

---

Before we get into navigation, we must do the Estimate initial pose by clicking on 2D Pose estimate in RVis and drag the green arrow toward the direction where the Turtlebot3 is facing, because we need to make the TurtleBot3 in its correct location before running the navigation.

![02](https://user-images.githubusercontent.com/71232960/125881840-9af04790-c229-4011-b4f6-47898eeed90b.png)

![03](https://user-images.githubusercontent.com/71232960/125882283-05d46235-6ae7-4be2-80fc-7ea50d19165f.png)

We will repeat the step until the green lights (which they are a LDS sensor data) are close to each other.

To make precisely locate the robot on the map, we can use the keyboard to move it by this command in a new Terminal:

`$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch`

![04](https://user-images.githubusercontent.com/71232960/125882390-489341a8-78d6-477b-afb8-f447299a3113.png)

![05](https://user-images.githubusercontent.com/71232960/125882565-a312cb11-bf01-4b4e-bb5a-5c06a7d13242.png)

---

After we estimate the location correctly, we can close the keyboard teleoperation node.

Now we can click on 2D Nav Goal in the menu, then click on the map to any position that we want the TurtleBot3 to go to it.

![06](https://user-images.githubusercontent.com/71232960/125883007-52caed57-c047-47a3-9b51-1e21d26c6fdb.png)

we can see the TurleBot3 move to the goal.

![07](https://user-images.githubusercontent.com/71232960/125883049-03db86ac-9d6d-4a32-8622-d8659cf433a6.png)

![08](https://user-images.githubusercontent.com/71232960/125883106-b1dde286-9281-471d-9eb2-5aac3e2d3686.png)

Note: The root of the red arrow is the x, y coordinate of the destination, and the arrow direction represents the orientation.

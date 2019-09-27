# Robotics PF Localization Project

The presented work demonstrates the Adaptive Monte Carlo Localization(AMCL) technique and its complexity
for global position estimation through simulation and analysis. Two different robot models are considered for performance evaluation
and how the shape of the robot, location and number of sensors affect the localization is understood.

The project writeup "Project_Where_Am_I.pdf" discuss the details of the project in professional format

The entire workspace for the student created robot is named as: "Student_model_workspace" zip file. The robot urdf file/s,mesh file for laser sensor,world file/s and launch file/s including amcl.launch can be located under following folder:

Student_model_workspace\workspace\catkin_ws\src\udacity_bot

This project shows how AMCL technique effectively determines the pose of a mobile robot fusing camera and laser sensor data while the robot is in motion. Once robot’s current pose is determined, it can effectively plan its path for a new navigation goal.

For the purpose of the project ROS was used in Ubuntu OS, that launches a custom robot model in a Gazebo world and utilizes packages like AMCL and the Navigation Stack. These packages would accurately localize a mobile robot inside a provided map in the Gazebo and
RViz simulation environments. Then specific parameters corresponding to each package were tuned to achieve the best possible localization results. The picture file "AMCL Parameter List1.png" shows the list of updated parameters for the laser scanner and wheel encoder.

Successful localisation for 2 different robots are shown by the picture files:

robot reached goal12.png

robot reached goal22.png

Analysing the localization result(pose) it could be concluded that both the robots were successfully able to plan path and reach the goal pose. However, the time to reach the goal from the starting point varied between 2 types of robot. It took almost 5 minutes for both the robots to reach the goal from the starting point. Sometimes the robots were stuck by the obstacles and the parameters for cost map were tuned to find the optimum result for smooth navigation.

# RI-TP5-NOTER

# RI Arm Description Package

This package contains the URDF description of the RI arm robot.

## Dependencies

This package depends on the following ROS packages:

- rospy
- roscpp
- urdf
- std_msgs
- geometry_msgs
- sensor_msgs

Please make sure you have these packages installed and built in your catkin workspace.

## Launching the Robot

To launch the robot, use the following command:

```bash
source ~/catkin_ws/devel/setup.bash  # Replace with the path to your catkin workspace
roslaunch urdf_tutorial display.launch model:=robot.urdf




## Visualizing the Robot in RViz

After launching the robot using the provided launch file, RViz should start automatically and you should be able to see the robot model. If not, you may need to adjust some settings:

1. **Add RobotModel Display:** In the "Displays" panel, click the "Add" button, select "RobotModel" from the list, and click "OK". This will add a new display type for visualizing robot models.

2. **Set Fixed Frame:** In the "Global Options" section of the "Displays" panel, set the "Fixed Frame" to a frame that exists in your robot model. For example, if your robot model has a base link named "base_link", you can set the "Fixed Frame" to "base_link".

3. **Enable Interact Tool:** In the top toolbar, click the "Interact" tool (the icon looks like a white arrow with a green circle around it). This will allow you to interact with the robot model by clicking and dragging the interactive markers.

If you're still not seeing the robot model, make sure your ROS core is running and your robot description is correctly loaded into the parameter server. You can check this by running the following command in a new terminal:

```bash
rosparam get /robot_description

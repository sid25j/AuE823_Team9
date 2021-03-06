# Mapping and localization
This is the submission for the 7th assignment

## Package: **assignment_7**

### Files and folders:
- **launch:**
    >*turtlebot3_slam_navigation.launch:* Used to launch the gazebo world, slam (default: gmapping), and teleop  

- **videos:**
    >*part2_sim_hokuyo_slam-2022-03-31_00.22.50.mp4:* shows the execution of the slam with hokuyo lidar  
    
    >*part2_sim_lds_slam-2022-03-31_00.33.41.mp4:* shows the execution of the slam with turtlebots' lidar  
    
- **maps**
    >*map2.pgm*: map generated using hokuyo lidar  
    ![github image](https://github.com/sid25j/AuE823_Team9/blob/main/catkin_ws/src/assignment_7/images/hokuyo.png)  
    >*map1.pgm*: map generated using lds lidar  
    ![github image](https://github.com/sid25j/AuE823_Team9/blob/main/catkin_ws/src/assignment_7/images/lds.png)
    
- **xacro_files:**
    >Contains two xacro files (*turtlebot3_burger.gazebo.xacro & turtlebot3_burger.urdf.xacro) should be placed in /opt/ros/noetic/share/turtlebot3_description/urdf/ 

    **To use the hokuyo lidar in simulation, edit the "turtlebot3_burger.gazebo.xacro" with a value of "1" for argument "is_using_hokuyo"**  
    > Example 1: <xacro:arg name="is_using_hokuyo" default="0"/>  # for using lds lidar  
      Example 1: <xacro:arg name="is_using_hokuyo" default="1"/>  # for using hokuyo lidar
    
### Execution:
**SLAM simulation:**
  - Using the launch file:
  > $ roslaunch assignment_7 turtlebot3_slam_navigation.launch
  
  - Saving the map:
  > $ rosrun map_server map_saver -f (file location)/(file name)  
  Example: $ rosrun map_server map_saver -f /home/sachetk/slam_maps_assignment_7/map2



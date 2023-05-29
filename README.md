# ROSarmdevelopment
Create and initialize a working directory
```
mkdir -p ~/duco_ws/src
cd ~/duco_ws/src
catkin_init_workspace
cd ~/duco_ws/
catkin_make
```
Download the installation package and unzip it
After decompression, copy the obtained source code to the specified /duco_ws/src
Specific code directory structure:

duco_ws
      --src
             --CMakeLists.txt
             --duco_controller
             --duco_demo
             --duco_driver
             --duco_gcr5_moveit_config
             --duco_msgs
             --duco_support
Compile source code
   ```
cd ~/duco_ws
source ./devel/setup.bash
catkin_make
   ```

Startup script
Start the robot controller program
Open terminal 1
```
cd ~/duco_ws
source ./devel/setup.bash
roslaunch duco_gcr5_moveit_config moveit_planning_execution.launch robot_ip:=192.168.*.* 
```

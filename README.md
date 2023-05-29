# ROSarmdevelopment
创建并初始化工作目录
```
mkdir -p ~/duco_ws/src
cd ~/duco_ws/src
catkin_init_workspace
cd ~/duco_ws/
catkin_make
```
下载安装包并解压
解压后将所得的源码复制到指定的/duco_ws/src下

具体代码目录结构：

duco_ws
      --src
             --CMakeLists.txt
             --duco_controller
             --duco_demo
             --duco_driver
             --duco_gcr5_moveit_config
             --duco_msgs
             --duco_support
   编译源代码
   ```
   cd ~/duco_ws
source ./devel/setup.bash
catkin_make
   ```
              启动脚本
启动机器人控制器程序
打开终端1
   ```
   cd ~/duco_ws
source ./devel/setup.bash
roslaunch duco_gcr5_moveit_config moveit_planning_execution.launch robot_ip:=192.168.*.*
   
      ```

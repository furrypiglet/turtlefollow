# 乌龟追逐_ROS实训（无循迹）

***

## 环境

Ubuntu20.04.6 LTS；ROS Noetic

## 功能

1. 利用`turtlesim`库创建两只乌龟，分别为`turtle1`和`turtle2`；
2. 利用`teleop`在控制台通过键盘上的方向键控制`turtle1`的移动；
3. 使`turtle2`自动追逐`turtle1`的位置（无循迹）并播报实时位置。

## 默认快速启动

1. 在控制台输入`roslaunch follow start_follow_c++.launch`，乌龟追逐开始运行；

2. 在控制台输入:arrow_up::arrow_down::arrow_left::arrow_right:指令控制`turtle1`运动，`turtle2`自动追逐。

## 普通启动

1. 在控制台1输入：

```
cd ~/catkin_ws
catkin_make
source devel/setup.bash
roscore
```

2. 在控制台2输入：

```
rosrun turtlesim turtlesim_node
```

3. 在控制台3输入：

```
rosrun follow turtle_tf_bc __name:turtle1_tf_broadcaster /turtle1
```

4. 在控制台4输入：

```
rosrun follow turtle_tf_bc __name:turtle2_tf_broadcaster /turtle2
```

5. 在控制台5输入：

```
rosrun follow turtle_tf_ln
```

6. 在控制台6输入：

```
rosrun turtlesim turtle_teleop_key
```

7. 在控制台输入:arrow_up::arrow_down::arrow_left::arrow_right:指令控制`turtle1`运动，`turtle2`自动追逐。

## 参考连接

1. ROS tutorial： http://wiki.ros.org/
2. 古月居教程：https://www.bilibili.com/video/BV1zt411G7Vn?p=1




# DAY3

## Rqt图形化的调试工具

* rqt is a software framework of ROS that implements the various GUI tools in the form of plugins. 
* 话题发布工具
* 摄像头画面查看工具
* rqt_plot绘图工具（rqt-Plugins-Visuallization-Plot）
* rqt         开启rqt
* rqt_graph
* 根据目标位置而改变横总坐标

## move base路径规划

* move base实现了自主导航当给予固定目标的时候
* global planer 确定了初始的行驶轨迹
* local planer 作出灵活改变当遇到突发情况
* global costmap 考虑全局代价
* local costmap 考虑临时代价
* recovery behavior 备用方案

## Example SLAM

* 启动gazebo环境包
* roslaunch turtlebot_gazebo turtlebot_world.launch 
* roslaunch turtlebot_gazebo gmapping_demo.launch 
* 启动控制
* roslaunch turtlebot_teleop keyboard_teleop.launch
* 查看地图
* roslaunch turtlebot_rviz_launchers view_navigation.launch

* 打开rqt_plot查看变化
* //roslaunch mx_urdf gazebo.launch另一个环境包

## 实际操作

* roslaunch mx_bringup rbc_lidar_start.launch
* roslaunch mx_nav gmapping_demo.launch
* roslaunch mx_rviz gmapping_view.launch 

## Movebase参数
* 参数: max_vel_x              机器人最大速度
* 参数: min_vel_x              机器人最小速度
* 参数: escape_vel             逃逸速度
* 参数: yaw_goal_tolerance     目标地点偏角容错
* 参数: xy_goal_tolerance      目标地点位置容错
* 参数: pdist_scale            局部规划置信度
* 参数: gdist_scale            全局规划置信度
* 参数: vx_samples             线速度采样点
* 参数: vtheta_samples         角速度采样点

## 其他

* ~/mxBot_ws/src/mx_turtleBot/mx_bringup/Show地图存放文件夹
* /home/intel/mxBot_ws/src/mx_turtleBot/mx_nav/config/fake网站




# DAY2

## Github注册
* 申请帐号
* 配置用户

## 创建仓储&推送学习笔记

* git clone                      克隆远程仓储
* git status                     查看仓储状态
* git add .                      记录在案
* git commit -m "(name)"         仓储加备注
* git pull                       拉远程仓储
* git push                       推远程仓储
* git dif                        查看改动
* //git是本地搭建；github是云端平台

## ROS框架

* 发布者——>话题——>订阅者 (ROS Master与ROS node的关系)
* ROS节点               rosnode info //rosnode displaying debug information about ROS Nodes, including publications, subscriptions and connections

* ROS消息               rosmsg show //displaying information about ROS Message types
* ROS话题               rostopic info

## rostopic指令

* rostopic bw	        display bandwidth used by topic
* rostopic delay	display delay of topic from timestamp in header
* rostopic echo	        print messages to screen
* rostopic find   	find topics by type
* rostopic hz	        display publishing rate of topic
* rostopic info	        print information about active topic
* rostopic list	        list active topics
* rostopic pub	        publish data to topic
* rostopic type   	print topic or field type

## 建立ROS工作空间

* 建立文件夹                        mkdir (name)_ws/src
* 进入src文件夹                     cd src
* 初始化工作空间                    catkin_init_workspace
* 回到初始文件夹                    cd ..
* 编译&加入bashrc自动加载环境       catkin_make

## 创建ROS功能包

* 进入src文件夹                     cd src
* 创建一个功能包                    catkin_ creat_pkg (name) rospy 
* 进入功能包                        cd (name)
* 创建launch文件并编辑              gedit (name).launch
* 运行launch功能包                  roslaunch (name).launch 

# DAY1

## 终端指令

* Ctrl+Alt+Shift+T              启动终端
* （已有终端时）Ctrl+Shift+T     合并终端
* pwd                           查看根目录
* cd                            进入文件夹
* /                             根目录
* ~                             用户 (cd = cd~ = cd Desktop/intel/ )
* cd ..                         返回上级目录
* cd -                          返回上次目录
* ls                            查看文件夹的内容
* ls -a                         查看所有文件
* mkdir (name)                  创建文件夹
* mkdir (name) (name) (name)    创建三个文件夹
* mkdir (name)/(name)/(name) -p 创建嵌套的三个文件夹
* mkdir (name)\ (name)          创建文件夹的名字里带空格
* vi                            没有桌面时更改文件（Esc Shift+; wq + Enter） 
* touch (name)                  创建文件
* man                           注释
* wq                            退出
* gedit                         更改文件
* rm                            删除文档
* rm -r (name)                  删除文件

## Color Follower

* 开启底盘
* roslaunch mx_bringup rbc_camera_start.launch
* 开启颜色追踪
* roslaunch mx_apps opencv3_follower.launch color

## Mapping Follower

* 开启底盘
* roslaunch mx_bringup rbc_camera_start.launch
* 开启建图模式
* roslaunch mx_nav gmapping_demo.launch

## 深度跟随

* 开启底盘
* roslaunch mx_bringup rbc_camera_start.launch
* 启动PCL点云追踪follower
* roslaunch mx_apps follower2.launch






# Airobot
Home service robots
############################## 描述
This is ouer home service robot code by ROS!

1.Drivers
   ROS arduino bridge,use mega2560 mcu,two pwm output driver for motor ,PID ctrl, ... ...
   
2.SLAM
   kinect 2.0 ... ...
   
3.Speech Recognition and Synthesis
   xunfei ... ...
############################## github
#upload上传数据
git add .
git commit -m "修改记录"
git push origin master
#updata更新数据
git pull
############################## 重要网页收藏
http://www.ncnynl.com/archives/201702/1287.html  //讯飞在线语音合成和识别  
https://zhidao.baidu.com/question/650798520162536005.html?fr=iks&word=htk%D3%EF%D2%F4%CA%B6%B1%F0&ie=gbk //常见语音识别
http://blog.csdn.net/u011272513/article/details/52139060 //Ubuntu 启动/引导修复


############################## 命令说明
#讯飞在线语音合成和识别
rosrun xfei_asr  tts_subscribe_speak
rostopic pub xfwords std_msgs/String "测试ncnynl.com"

rosrun xfei_asr  iat_publish_speak
rostopic echo /xfspeech
rostopic echo /xfwords
rostopic pub xfwakeup std_msgs/String "ok"

#常用ROS命令
rosrun rosserial_python serial_node.py /dev/ttyUSB0

rosrun turtlesim turtlesim_node
rosrun turtlesim turtle_teleop_key

roslaunch kinect2_bridge kinect2_bridge.launch
rosrun kinect2_viewer kinect2_viewer

rostopic bw     display bandwidth used by topic
rostopic echo   print messages to screen
rostopic hz     display publishing rate of topic
rostopic list   print information about active topics
rostopic pub    publish data to topic
rostopic type   print topic type

rostopic list -v
rosmsg show [topic]
roslaunch rbx1_bringup fake_turtlebot.launch
rosrun rviz rviz -d `rospack find rbx1_nav`/interactive_markers.rviz

source /opt/ros/kinetic/setup.bash
source devel/setup.bash
source ./devel/setup.bash

catkin_create_pkg <package_name> [depend1] [depend2] [depend3]
#catkin_create_pkg beginner_tutorials std_msgs rospy roscpp

rospack depends <package_name>
#rospack depends beginner_tutorials 

rospack depends1 <package_name>
#rospack depends1 beginner_tutorials 

rosrun rqt_graph rqt_graph

#uart
dmesg | grep ttyUSB0
lsmod | grep usbserial
sudo cutecom
sudo putty
sudo serialhelper


roslaunch ros_arduino_python arduino.launch

rosrun tf view_frames
evince frames.pdf











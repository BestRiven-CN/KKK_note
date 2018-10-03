## DAY4

## 桌面的一张图片如何变成黑白的
<code>
import cv2

img=cv2.imread('/home/intel/Desktop/image.jpeg',0)

cv2.imshow("Display",img)

cv2.waitKey(1000)

cv2.imwrite("imagegray.jpeg",img)

cv2.destroyALLWindows()
</code>

## 摄像头
<code>
import numpy as np
import cv2

cap = cv2.VideoCapture(2)

while(True):
	ret, frame = cap.read()
	cv2.imshow('frame',frame)
	gray = cv2.cvtColor(frame,cv2.COLOR_BGR2GRAY)
	cv2.imshow('gray',gray)
	image90 = np.rot90(gray)
	cv2.imshow('gray-90',image90)
	rgb90 = np.rot90(frame)
	cv2.imshow('rgb-90',rgb90)
	if cv2.waitKey(1)& 0xFF == ord('q'):
		break

cap.release()
cv2.destroyAllWindows()
</code>

## Chatter内容
<code>
import rospy
from std_msgs.msg import String

def talker():
   pub = rospy.Publisher('chatter',String,queue_size=10)
   rospy.init_node('talker',anonymous=True)
   rate = rospy.Rate(10)
   
   while not rospy.is_shutdown():
      hello_str = "hello ROS %s" % rospy.get_time()
      rospy.loginfo(hello_str)
      pub.publish(hello_str)
      rate.sleep()

if __name__ == '__main__':
   try:
      talker()
   except rospy.ROSInterruptException:
      pass
</code>

## 让自己的车自动走
<code>
import rospy
from geometry_msgs.msg import Twist

xue_pub = rospy.Publisher('/cmd_vel',Twist,queue_size=1)
rospy.init_node('xuehenxiaowugui')
xuegai_rate =rospy.Rate(5)

while not rospy.is_shutdown():
   Antisociety_cmd = Twist()
   Antisociety_cmd.linear.x = 0.4
   Antisociety_cmd.angular.z = 0.8

   xue_pub.publish(Antisociety_cmd)

   xuegai_rate.sleep()
</code>

## 机器人移动并给出反馈
<code>
import rospy
from std_msgs.msg import String
from geometry_msgs.msg import Twist 

def callback(xue):
   if (xue.linear.x>0):
      rospy.loginfo("w")
   if (xue.linear.x<0):
      rospy.loginfo("s")
   if (xue.angular.z>0):
      rospy.loginfo("a")
   if (xue.angular.z<0):
      rospy.loginfo("d") 

  
   
def listener():

   rospy.init_node('listener',anonymous=True)
   rospy.Subscriber("cmd_vel",Twist,callback)
   rospy.spin()

if __name__ == '__main__':
   listener()
</code>

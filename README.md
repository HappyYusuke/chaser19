**********************************************
*** KES version                            ***
*** A follow human program by Kosei Demura *** 
**********************************************

Change log: 
2018-08-10: Fixed CMakeLists.txt for OpenCV 3.0.

ToDo:
衝突回避機能を実装する
追跡範囲外に出ると止まる問題。追跡範囲を広げるなど。


Thiss program finds human by using the Hokuyo UTM-30LX lidar.

1. Environment  
   Ubuntu14.04 and ROS Iindigo

2. Build  
   $ cd ~/catkin_ws  
   $ catkin_make

3. Run  
   (1) Launch with other nodes  
   $ rosrun follow_human follow_human  

   (2) Stand-alone  
   $ roscd chaser  
   $ cd script  
   $ ./chaser.sh  

4. Topic   
  (1) Publish   
      name: find_human   
      type: std_msg/String   
      value: "true", "false"  
       
  (2) Subscribe   
      name: follow_human  
      type: std_msg/String  
      value: "start", "stop", "none"
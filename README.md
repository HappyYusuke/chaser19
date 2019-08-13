**********************************************
*** KES & OpenCV3 対応バージョン            ***
*** A follow human program by Kosei Demura *** 
**********************************************


**概要**  
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
   $ ./chaser_alone.sh  

4. Topic   
  (1) Publish   
      name: /find_human   
      type: bool
      value: "true", "false"  
       
  (2) Subscribe   
      name: /follow_human  
      type: std_msgs/String  
      value: "start", "stop", "none"

**Change Log**  
2018-08-13: chaser19.cppを@Home競技に対応させた。/follow_humanトピックによりstart、stopできる。
2018-08-10: Fixed CMakeLists.txt for OpenCV 3.0.  

**ToDo**    
1.衝突回避機能を実装する  
2. 追跡範囲外に出ると止まる問題。追跡範囲を広げるなど。　

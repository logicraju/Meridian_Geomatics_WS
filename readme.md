# Manual Mapper using Lidar, IMU and GPS

## Setup Procedure
 1. rosdep install --from-paths src --ignore-src -r -y
 2. sudo apt install libpcap-dev libyaml-cpp-dev
 3. sudo apt install python3-catkin-tools
 4. catkin build
 5. Set static IP as 192.168.1.100 and subnet mask to 255.255.255.0 in the computer so as to enable communication with Lidar
    ![Network Setup](https://github.com/logicraju/Meridian_Geomatics_WS/blob/main/Resources/Network%20Setup.png)
    
    For troubleshooting Lidar IP issues:
    [![Watch](https://img.youtube.com/vi/Y3ZYh9g4TtU&ab_channel=HesaiTechnology/0.jpg)](https://www.youtube.com/watch?v=Y3ZYh9g4TtU&ab_channel=HesaiTechnology)
 
 6. Check the data packets using Wireshark. To install Wireshark:
    'sudo apt update
     sudo apt install wireshark
     (Allow non-super users to capture packets)'

 7. Set the name of lidar as XT32 in launch file
    >Refer: src/HesaiLidar_General_ROS/launch/hesai_lidar.launch
   
   
   
### Note: Sometimes, catkin build command needs to be run twice consecutively to build

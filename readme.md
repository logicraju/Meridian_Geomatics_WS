# Manual Mapper using Lidar, IMU and GPS

## Hesai Lidar - Setup Procedure
 1. Set static IP as 192.168.1.100 and subnet mask to 255.255.255.0 in the computer so as to enable communication with Lidar
    ![Network Setup](https://github.com/logicraju/Meridian_Geomatics_WS/blob/main/Resources/Network%20Setup.png)
    
    For troubleshooting Lidar IP issues:
    [![Watch](https://img.youtube.com/vi/Y3ZYh9g4TtU&ab_channel=HesaiTechnology/0.jpg)](https://www.youtube.com/watch?v=Y3ZYh9g4TtU&ab_channel=HesaiTechnology)
 
 2. Check the data packets using Wireshark. To install Wireshark:
    'sudo apt update
     sudo apt install wireshark
     (Allow non-super users to capture packets)'

 3. Set the name of lidar as XT32 in launch file
    >Refer: src/HesaiLidar_General_ROS/launch/hesai_lidar.launch
   

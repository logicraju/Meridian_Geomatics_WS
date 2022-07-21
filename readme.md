# Manual Mapper using Lidar, IMU and GPS

## Hesai Lidar - Setup Procedure
 1. Set static IP as 192.168.1.100 and subnet mask to 255.255.255.0 in the computer so as to enable communication with Lidar
    ![Network Setup](https://photos.app.goo.gl/igq3kQQhTSoQqU5y5)
 
 2. Check the data packets using Wireshark. To install Wireshark:
    'sudo apt update
     sudo apt install wireshark
     (Allow non-super users to capture packets)'

 3. Set the name of lidar as XT32 in launch file
 
 `<launch>
	  <arg name="pcap_file"  default=""/>
	  <arg name="server_ip" default="192.168.1.201"/>
	  <arg name="lidar_recv_port"  default="2368"/>
	  <arg name="gps_port"  default="10110"/>
	  <arg name="start_angle"  default="0"/>
	  <!--“lidar_type” represents the model of the lidar-->
	  <arg name="lidar_type" default=""/>
	  <!--"frame_id" represents the id of the point cloud data published to ROS-->
	  <arg name="frame_id" default=""/>
	  <arg name="pcldata_type" default="0"/>
	  <arg name="publish_type" default="points"/>
	  <arg name="timestamp_type" default=""/>
	  <arg name="data_type" default=""/>
	  <arg name="namespace" default="hesai"/>
	  <arg name="lidar_correction_file"  default="$(find hesai_lidar)/config/Pandar64.csv"/>
	  <arg name="multicast_ip"  default=""/>
	  <arg name="coordinate_correction_flag"  default="false"/>
	  <arg name="fixed_frame"  default=""/>
	  <arg name="target_frame"  default=""/>
     
	  <node pkg="hesai_lidar" name="hesai_lidar" ns="$(arg namespace)" type="hesai_lidar_node" output="screen" >
		  <param name="pcap_file" type="string" value="$(arg pcap_file)"/>
		  <param name="server_ip" type="string" value="$(arg server_ip)"/>
		  <param name="lidar_recv_port"  type="int" value="$(arg lidar_recv_port)"/>
		  <param name="gps_port"  type="int" value="$(arg gps_port)"/>
		  <param name="start_angle"  type="double" value="$(arg start_angle)"/>
		  <param name="lidar_type"  type="string" value="$(arg lidar_type)"/>
		  <param name="frame_id"  type="string" value="$(arg frame_id)"/>
		  <param name="pcldata_type"  type="int" value="$(arg pcldata_type)"/>
		  <param name="publish_type"  type="string" value="$(arg publish_type)"/>
		  <param name="timestamp_type"  type="string" value="$(arg timestamp_type)"/>
		  <param name="data_type"  type="string" value="$(arg data_type)"/>
		  <param name="lidar_correction_file"  type="string" value="$(arg lidar_correction_file)"/>
		  <param name="multicast_ip"  type="string" value="$(arg multicast_ip)"/>
		  <param name="coordinate_correction_flag"  type="bool" value="$(arg coordinate_correction_flag)"/>
		  <param name="fixed_frame"  type="string" value="$(arg fixed_frame)"/>
		  <param name="target_frame"  type="string" value="$(arg target_frame)"/>
	  </node>
  </launch>`


    
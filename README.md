# ArduROS

DEV NOTES - DO NOT USE


Clone to GitHub Folder
Move to installmavros folder
sudo apt-get update
sudo ./installROSwMAVROS.sh -p ros-kinetic-desktop-full
 
_________________________________________________
Install APSync

Install ROS

ssh -X apsync@10.0.1.128

Install ROS Pkgs

sudo apt-get install python-rosinstall python-rosinstall-generator python-wstool python-catkin-tools build-essential -y

 echo "source /home/apsync/catkin_ws/devel/setup.bash" >> ~/.bashrc
source ~/.bashrc

cp /home/apsync/catkin_ws/src/aion_r1/r1_control/config/mavlink-router.conf /home/apsync/start_mavlink-router

/opt/ros/kinetic/lib/mavros$ sudo ./install_geographiclib_datasets.sh 

mavproxy.py --mav10 --master :14550 --source-system=89

Add GUIDED MODE

/mavros/setpoint_velocity/cmd_vel
geometry_msgs/Twist

[UdpEndpoint to_172_14550]



  <!-- Joystick Interface Launch  -->
  <!--
  <arg name="joy_config" default="ps3" />
  <arg name="joy_dev" default="/dev/input/js0" />
  <arg name="config_filepath" default="$(find teleop_twist_joy)/config/$(arg joy_config).config.yaml" />

  <rosparam command="load" file="$(find r1_control)/config/teleop.yaml" />

      	<node pkg="joy" type="joy_node" name="joy_node">
          	<param name="dev" value="$(arg joy_dev)" />
          	<param name="deadzone" value="0.3" />
          	<param name="autorepeat_rate" value="20" />
        </node>

        <node pkg="teleop_twist_joy" name="teleop_twist_joy" type="teleop_node">
        </node> -->


/cmd_vel
/diagnostics
/mavlink/from
/mavlink/to
/mavros/battery
/mavros/extended_state
/mavros/global_position/compass_hdg
/mavros/global_position/global
/mavros/global_position/gp_lp_offset
/mavros/global_position/gp_origin
/mavros/global_position/home
/mavros/global_position/local
/mavros/global_position/raw/fix
/mavros/global_position/raw/gps_vel
/mavros/global_position/rel_alt
/mavros/global_position/set_gp_origin
/mavros/home_position/home
/mavros/home_position/set
/mavros/imu/data
/mavros/imu/data_raw
/mavros/imu/diff_pressure
/mavros/imu/mag
/mavros/imu/static_pressure
/mavros/imu/temperature_baro
/mavros/imu/temperature_imu
/mavros/local_position/odom
/mavros/local_position/pose
/mavros/local_position/velocity
/mavros/manual_control/control
/mavros/manual_control/send
/mavros/mission/reached
/mavros/mission/waypoints
/mavros/radio_status
/mavros/rc/in
/mavros/rc/out
/mavros/rc/override
/mavros/setpoint_accel/accel
/mavros/setpoint_attitude/cmd_vel
/mavros/setpoint_attitude/thrust
/mavros/setpoint_position/global
/mavros/setpoint_position/local
/mavros/setpoint_raw/attitude
/mavros/setpoint_raw/global
/mavros/setpoint_raw/local
/mavros/setpoint_raw/target_attitude
/mavros/setpoint_raw/target_global
/mavros/setpoint_raw/target_local
/mavros/setpoint_velocity/cmd_vel
/mavros/state
/mavros/statustext/recv
/mavros/statustext/send
/mavros/time_reference
/mavros/timesync_status
/mavros/vfr_hud
/mavros/wind_estimation
/rosout
/rosout_agg
/tf
/tf_static

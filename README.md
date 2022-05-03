# MARV-ROS-WITH-RNS
ROS software for the MARV system with Remote Network Steering scenario.
Have a look at the README of the original repository for more information on the ROS system.


# Start RNS
## ROS 2
Start ROS by running the marv_start shell script.
Make sure that the workspace is built with no errors using "colcon build --symlink-install"

## Web server
The operator controls the MARV using an XBOX controller and a web interface served by the web server. To launch this:
- Source ROS 2 Eloquent ("source /opt/ros/eloquent/setup.bash")
- Locate the server folder ("cd Documents/MARV-ROS-WITH-RNS/WEB-UI/dist")
- Start the server using "node server.js". Might want to do this differently in the future, for example with the PM2 daemon.
- Open a web browser (preferrably Chrome based) and go to the IP address of the REACH computer (192.168.1.92 in the CASE lab) and add port 1337 to the end, like this "192.168.1.92:1337"
- Press "Enable Gamepad" and you are ready to steer the MARV
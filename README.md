# MARV-ROS-WITH-RNS
ROS software for the MARV system with Remote Network Steering scenario.
Have a look at the README of the original repository for more information on the ROS system.

# Start RNS
## ROS 2
Install everything as mentioned in "reach setup" in the original repository this one is forked from.
Make sure that the workspace is built with no errors using "colcon build --symlink-install".

Start ROS by running the marv_start shell script ("./marv_start.sh").

## Web server and ROS node (in one package)
The operator controls the MARV using an XBOX controller and a web interface served by the web server. 

Before you can run the server you need to install Node.js, preferrably version 16 since the server was only developed and tested with this version. Node version manager (NVM) works well for installing a specific Node version on the REACH computer.
Then you need to install all npm dependencies for the server. This can be done by running "npm install" inside the "WEB-UI" folder. 

After the installation, launch the server like this:
- Source ROS 2 Eloquent ("source /opt/ros/eloquent/setup.bash")
- Locate the server folder ("cd Documents/MARV-ROS-WITH-RNS/WEB-UI/dist")
- Start the server using "node server.js". The ROS node is baked into the server.js script and will start simultaneously with the server. Might want to do this differently in the future, for example with the PM2 daemon.
- Open a web browser (preferrably Chrome based) and go to the IP address of the REACH computer (192.168.1.92 in the CASE lab) and add port 1337 to the end, like this "192.168.1.92:1337"
- Press "Enable Gamepad" and you are ready to steer the MARV

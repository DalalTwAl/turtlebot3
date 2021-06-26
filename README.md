# turtlebot3
Welcome to the turtlebot3 wiki!

first we need to do the gazebo simulation part



https://emanual.robotis.com/docs/en/platform/turtlebot3/simulation/#gazebo-simulation



install the simulation package



$ cd ~/catkin_ws/src/



$ git clone -b melodic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git



$ cd ~/catkin_ws && catkin_make



launch simulation world we can pick between (burger, waffle) I picked waffle so it will be:



$ export TURTLEBOT3_MODEL=waffle



$ roslaunch turtlebot3_gazebo turtlebot3_world.launch



operate turtlebot3



$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch



the SLAM part



we need to launch the simulation world first, since we are using waffle



$ export TURTLEBOT3_MODEL=waffle



$ roslaunch turtlebot3_gazebo turtlebot3_world.launch



run SLAM node, here we need to open a new terminal



$ export TURTLEBOT3_MODEL=waffle



$ roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping



run teleoperation nod, a new terminal needed



$ export TURTLEBOT3_MODEL=waffle



$ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch



the map will show here but since I'm using a website it won't even after I did all the steps till the end



the last thing is saving the map after it appears



$ rosrun map_server map_saver -f ~/map

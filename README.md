# Autonomous Ball Picking and Lane Following Robot

This robot basically follows the middle lane of a road, and autonomously picks up green balls and avoids red balls throughout the map. It also Identifies road signs (left/right)
and turns in the appropriate direction.

link to the video - https://youtu.be/ncgQHx79Lvc

# Follow these steps to run :
contains the integration of line-follower,arrow_detection,laser,and ball pick-up and pushing code.
to use this, follow the steps below:

1) create a new workspace
2) make an src folder
3) catkin_make this workspace
4) replace the src folder you created with src_aryan folder from this repository
5) go to the world file in the env folder and change paths from '/aryan/final_ws' to your computers path name.
6) to launch the bot in gazebo run :- roslaunch bot1 controls.launch, and press the play button below to run the simulation in gazebo.
   you may face a error of differential drive,try this : sudo apt-get install ros-kinetic-diff-drive-controller
7) all the python codes are present in the scripts folder inside bot1 package
8) the important codes that you have to run for the bot to work are - arrow.py , image.py, in that order respectiviely in separate terminals
   using command rosrun bot1 <filename.py>
9) image.py contains the main code for line following and ball pickup/push , wherease arrow.py finds the direction of arrow and sends it to image .py through a topic, so that the bot turns in the specified direction when intersection occurs. ball_detection sends the color and centroid value of the nearest ball to image.py through a topic. so that image.py can make decision to pickup/push ball if red/green and ball following with help of centroid. 
10) note - if laser value <23cm bot will stop.

![alt text](https://github.com/arubittu/UMIC_autonomous_bot_team4/blob/master/BOT%20PICS/1.png?raw=true)


## Running the package
##### 1. Clone this package inside the _src_ folder of your catkin workspace and run the ___catkin_make___ command.
##### 2. Change the path of custom plugin _.so_ file at the end of the following file: _SDF/model.sdf_
##### 3. Enter the following command in your terminal to run this tutorial: ___roslaunch differential_drive_tutorial diff_drive.___

## Structure of the package
##### 1. The SDF folder contain the differential drive robot model designed on the Gazebo Model Editor. Read the comments in the sdf to understand basic elements of a robot model in Gazebo.
##### 2. The src folder contains the source code of our custom plugin. Read the comments in the code to understand the elements of a custom plugin.
##### 3. The catkin_make command compiles this plugin source code into a shared object file and saves it at the following path: _catkin_ws/devel/lib/libdifferential_drive_tutorial.so_
##### 4. The launch folder consists the launch file to run Gazebo and spawn our model into the empty_world. You can also run any other ROS node through this single launch file.

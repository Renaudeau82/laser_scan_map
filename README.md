# laser_scan_map

To create the map using the laser scans and odomotry, I used Gmapping package.

### Prerequisites
Gmaping is not pushed on ros melodic yet, but the sources are working.
To save the map, you will need map_server package.

### Installing Gmapping
Steps to unstall all the dependances.
Somes are not on ros melodic yet and need to be built.
Use a git clone command in a catkin ready workspace/src 

* Gmapping [sources](https://github.com/ros-perception/openslam_gmapping)
* openslam_gmapping [sources](https://github.com/ros-perception/openslam_gmapping)

the "catkin_make" command will try to build everything.

To build these sources you may need dependances. They are all available on melodic. 
A "sudo apt--get instal ros-melodic-..." will do the job

### Installing mar_server
This package is said to be avaible directly. It is but the install went wrong for me.
You can also install it using the sources

* navigation [sources](https://github.com/ros-planning/navigation)

To build this sources you may need dependances. They are all available on melodic. 
A "sudo apt--get instal ros-melodic-..." will do the job

## Running the tests
This slam was tested on a rosbag with well named topic.

The launch file used is avaiable in the repository: test_wyca.launch
(it uses a rviz config file)

To save the map, use the command "rosrun map_server map_saver -f map" to obtain an image of the map.
The image is a .pgm file that you can turn into a .png file using gimp.

The result is presented in the figure below
![map](https://github.com/Renaudeau82/laser_scan_map/blob/master/map_wyca.png)

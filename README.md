# Exploration frontier 2D Doc Support
On this repository can you find the figures and data using the Bachelor thesis Autonomous Simultaneous Localization and Mapping by Dan Nykjær Jakobsen, in which the ros
package exploration_frontier_2d is created. 

This repository contains: 
 - Figures from rapport named according to the figure number in the folder rapport_figures
 - Data used in the two test under the folder data. 
 - The raw data obtains from simulations in the folder raw_data
 - Gif created the map from the raw data to show the progress of the simulation, in folder gif


## Testing environment 
On the link [enviroment](https://drive.google.com/file/d/1pOkoxbU8qE7XICGPc0hDa-PY7J1W0V6d/view?usp=sharing) you can find a image for [LXD contianer](https://linuxcontainers.org/lxd/introduction/). This contains all the complete testing environment, such as the different ROS package and gazebo world files. This image requires to the default profile together with gui and modules. The gui profile allows the packages to open gui elements, and the modules gives the container access to the kernel module, only in read mode. This profiles can be found on [TheWorldOfCode/LXD](https://github.com/TheWorldOfCode/LXD). 

In order to create a container with this image, run the following code
``` bash
lxc image import exploration_frontier_2d_environment 
lxc launch exploration_frontier_2d mycontainer
```
Where mycontainer is the name of the new container.

In order enter the container 
``` bash
pulseaudio --start 
lxc start mycontainer
lxc exec mycontainer -- sudo --user ubuntu --login
```
The first two lines are only need when the container is not running 

---
layout: default
---

# Welcome to the <u>Mo</u>bile <u>Man</u>ipulation <u>Tu</u>torial (MoManTu). 

This is the webpage for the tutorial in the (journal to be announced). Find the overview paper here (link to open access paper provided once it is accepted) and the detailed tutorial here (dito). 

The tutorial teaches how to program a mobile robot with a robot arm to do mobile manipulation. The example systems are a [Fetch](https://fetchrobotics.com/robotics-platforms/) robot and a [Clearpath Jaca](https://clearpathrobotics.com/jackal-small-unmanned-ground-vehicle/) with a [Kinova Jaco](https://www.kinovarobotics.com/en/products/gen2-robot) attached - see the image below.

<img src="/imgs/robots.jpg" alt="MoManTu Robots" width="50%"/>

The tutorial is developed by the [Mobile Autonomous Robotic Systems Lab](https://robotics.shanghaitech.edu.cn/) (MARS Lab) and the [Living Machines Lab](http://lima.sist.shanghaitech.edu.cn/) (LiMa Lab) of the [ShanghaiTech Automation and Robotics Center](http://star-center.shanghaitech.edu.cn/) (STAR Center), [School of Information Science and Technology](http://sist.shanghaitech.edu.cn/) (SIST) of [ShanghaiTech University](https://www.shanghaitech.edu.cn/). 

Below two videos show the demo on a real and a simulated Fetch robot:

<video width="100%" controls>
  <source src="/videos/real_fetch_web.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

<video width="100%" controls>
  <source src="/videos/sim_fetch_web.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>

&nbsp;  

# Docker

The easiest way to get started with playing with the tutorial is to use the provided Docker image. 
    
To pull the docker image and run the demo use:

```bash
docker run --name momantu -i -t -p 6900:5900 -e RESOLUTION=1920x1080 yz16/momantu
```

Then open a VNC client (e.g. [RealVNC](https://www.realvnc.com/en/connect/download/viewer)) and connect to _127.0.0.1:6900_. The workspaces are located in the root folder and ready to use. 

## Run MoManTu

Launch the simulator and the MoManTu software by running this command in the terminal:

```bash
roslaunch fetch_sim demo.launch
```

The pose estimation module based on NOCS, which runs under a conda environment of Python 3.5.
Activate the environment and launch the object pose estimation module with:
```bash
conda activate NOCS #activate environment
source ~/nocs_ws/devel/setup.bash
roslaunch nocs_srv pose_estimation_server.launch
```

Finally, launch the flexbe_app and robot_server node to connect other modules and start the demo: 
```bash
roslaunch fetch_sim robot_service.launch
```

# Sources

The sources for the MoManTu are on GitHub: [https://github.com/momantu](https://github.com/momantu).

# Getting Help

You are welcome to post issues on the [momantu fetch](https://github.com/momantu/momantu_fetch/issues) repo to get help. You may also send an email to [Hou Jiawei](mailto:houjw@shanghaitech.edu.cn?subject=[GitHub]%20MoManTu) or [Prof. Sören Schwertfeger](mailto:soerensch@shanghaitech.edu.cn?subject=[GitHub]%20MoManTu).

# Sensor Log

A ROS bagfile with the sensor data from a real fetch run is [avaiable](https://robotics.shanghaitech.edu.cn/static/datasets/MoManTu/fetch_real.bag) (3.4GB).

# Citing

Please cite our paper if you use the tutorial in your research.

(bibtex citation to be provided)



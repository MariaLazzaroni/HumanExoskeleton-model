HumanExoskeleton-model
===========
SDF and URDF models for simulation of the human and the exoskeleton in Gazebo.

Models
------------
* Human URDF model: the human body is modeled as an articulated multi-body system with links connected by joints. Links has simple geometric shapes (parallelepiped, cylinder, sphere). Each joint has 1,2 or 3 DOFs (see [here](https://github.com/claudia-lat/MAPest/commit/f2b7a0b7f1cd0f1ee953f21e1c57b075005eee10) a description of each joint allowed movements). It is worth to note that we consider 1-DoFs revolute joints and combination of them to obtain a series of joints with a higher number of DoFs. As a straightforward consequence, this choice implies the presence of 'fake' links (denoted in the templates with *name-of-the-link_f*) with mass and dimensions negligible.

* Exoskeleton URDF model: this model is the result of a process of extraction of kinematics parameters, inertial parameters and meshes from the original CAD files of the RoboMate exoskeleton. For more information, see the [documentation](https://github.com/MariaLazzaroni/HumanExoskeleton-model/blob/master/misc/CADtoURDF.pdf).

* Human-Exoskeleton SDF model: is the model, referencing the other two URDF models, of the composite structure. 

Installation
------------
Install [YARP](http://www.yarp.it/install.html), [Gazebo](http://gazebosim.org/tutorials?cat=install) and  [gazebo-yarp-plugins](https://github.com/robotology/gazebo-yarp-plugins).

As HumanExoskeletonSDFmodel uses [YARP](http://yarp.it), remember to start it before starting the simulation, using the following command in a console:
```
yarpserver 
```

Then, run Gazebo for start the simulation.

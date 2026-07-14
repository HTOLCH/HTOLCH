## Harry Tolcher

Robotics and autonomy software engineer in Perth. C++ and Python on ROS 2, on the part of the stack
where planning and perception meet real hardware.

Mechanical engineer by degree (MPE, UWA), so I can design the mount as well as write the node that
reads the sensor bolted to it. Useful on a small team.

---

### Crowd-matching velocity planning for Autoware

*Master's thesis.* **[Code and write-up](https://github.com/HTOLCH/autoware_crowd_matching_module)**

<img align="right" width="240" src="https://raw.githubusercontent.com/HTOLCH/HTOLCH/c55ca539e05c5aed611e9554a42e448b9bbfe12b/media/nuway_shuttle.jpg" alt="The nUWAy autonomous shuttle, an EasyMile EZ10, on the UWA campus">

nUWAy is an EasyMile EZ10 on shared footpaths at UWA. Stock Autoware stops 5 m short of every
pedestrian it sees, so on a busy path it never gets anywhere. I wrote a `behavior_velocity_planner`
plugin that picks out the pedestrians walking with the bus, estimates the crowd's speed and matches
it, with proximity attenuation underneath so closing on the crowd never costs clearance. To test it I
built a pedestrian simulation environment in AWSIM with the crowd driven by a Social Force Model,
which doubled as the benchmark baseline. I also brought the full Autoware stack up on the shuttle's
own hardware, integrating it from a large and sparsely documented codebase, and built the lidar
perception that tracks pedestrians around it. Across a density sweep the planner removed stop events
entirely and held mean time-to-collision above 2.3 s. It was validated in simulation; the stack
deployment ran on the vehicle.

<br clear="all">

<p align="center">
  <sub>Left: RViz, with the live co-flow speed readout. Right: AWSIM.</sub>
  <br>
  <img src="https://raw.githubusercontent.com/HTOLCH/autoware_crowd_matching_module/3a5c5a85b04ad23f0823731d918c1b4ec0605e81/docs/media/demo.gif" width="540" alt="Crowd-matching velocity planning in AWSIM simulation">
</p>

<img align="right" width="300" src="https://raw.githubusercontent.com/HTOLCH/HTOLCH/5e4e5747df043f97b250a7852fb23a3c4f10b065/media/campus_pointcloud_perspective.png" alt="Lidar pointcloud map of the UWA campus, coloured by height">

It localises against a prior lidar map of campus: 1.25 million points over roughly 840 by 560 m, with
a lanelet2 vector map on top for the drivable paths.

<br clear="all">

---

### Autonomous navigation and SLAM, simulation to hardware

<img align="right" width="240" src="https://raw.githubusercontent.com/HTOLCH/HTOLCH/bf5e42aedf46f11bd433d1e001cfa649a16013cb/media/pioneer.jpg" alt="Pioneer robot with lidar and onboard compute">

GPS-waypoint navigation with a tuned Kalman filter over IMU, lidar and GPS, plus 3D SLAM. Built in
Gazebo, then deployed on a Pioneer robot outdoors, which is where the assumptions that only hold in
simulation tend to surface. Perception ran on PyTorch: object detectors to find targets around the
course, and a vision-based policy mapping camera images straight to steering.

<br clear="all">

---

### FPV drones

<img align="right" width="240" src="https://raw.githubusercontent.com/HTOLCH/HTOLCH/bf5e42aedf46f11bd433d1e001cfa649a16013cb/media/drone.jpg" alt="Custom-built 5 inch FPV quadcopter">

I design, build, repair and fly custom FPV quads. The one pictured is a 5 inch Armattan build.
Footage: **[youtube.com/@hazfpv771](https://www.youtube.com/@hazfpv771)**

<br clear="all">

---

### Technical

**Languages** C++, Python
**Robotics** ROS 2, Autoware, motion and velocity planning, SLAM, state estimation and sensor fusion (Kalman)
**Perception** Lidar tracking and object detection, PyTorch, OpenCV, YOLO
**Simulation** AWSIM / Unity, Gazebo, sim-to-real testing
**Mechanical** SolidWorks, Siemens NX, MATLAB/Simulink, vehicle dynamics, BOM ownership
**Electronics** Soldering, flight controllers, Raspberry Pi, motor characterisation, sensor integration
**Tooling** Linux, Git, Docker

Previously: internships in mining and energy, at First Mode on a hydrogen haul-truck retrofit and at
GPA Engineering on pipelines. I tutor Mobile Robots, and Risk, Reliability & Safety, at UWA.

---

Available now, and looking for graduate robotics and autonomy roles in Perth.

Perth, WA &nbsp;·&nbsp; [LinkedIn](https://www.linkedin.com/in/harry-tolcher-b69a65267/) &nbsp;·&nbsp; [YouTube](https://www.youtube.com/@hazfpv771) &nbsp;·&nbsp; harrytolcher1@gmail.com

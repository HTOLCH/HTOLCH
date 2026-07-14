## Harry Tolcher

Robotics and autonomy software engineer in Perth, Western Australia. C++ and Python, mostly on
ROS 2. I work on the part of the stack where planning and perception have to survive contact with
real hardware.

My degree is a Master of Professional Engineering (Mechanical) from UWA, so I can design the mount as
well as write the node that reads the sensor bolted to it. On a small team that tends to be useful.

---

### Crowd-matching velocity planning for Autoware

*Master's thesis.* **[Code, results and full write-up](https://github.com/HTOLCH/autoware_crowd_matching_module)**

<img align="right" width="260" src="https://raw.githubusercontent.com/HTOLCH/HTOLCH/c55ca539e05c5aed611e9554a42e448b9bbfe12b/media/nuway_shuttle.jpg" alt="The nUWAy autonomous shuttle, an EasyMile EZ10, on the UWA campus">

nUWAy is an EasyMile EZ10 running on shared footpaths at UWA. Stock Autoware stops 5 m short of
every pedestrian it sees, so on a busy path it never gets anywhere.

I wrote a `behavior_velocity_planner` plugin that picks out the pedestrians walking with the bus,
estimates the crowd's speed and matches it, with proximity attenuation underneath so closing on the
crowd never costs clearance. To test it I built a pedestrian simulation environment in AWSIM, with
the crowd driven by a Social Force Model, which doubled as the baseline I benchmarked against. I also
brought the full Autoware stack up on the shuttle's own hardware, and built the lidar perception that
tracks pedestrians around it.

Across a sweep of pedestrian densities it removed stop events entirely and held mean
time-to-collision above 2.3 s. Marked 87. The planner was validated in simulation; the stack
deployment was on the vehicle.

<br clear="all">

<p align="center">
  <img src="https://raw.githubusercontent.com/HTOLCH/autoware_crowd_matching_module/3a5c5a85b04ad23f0823731d918c1b4ec0605e81/docs/media/demo.gif" width="560" alt="Crowd-matching velocity planning in AWSIM simulation">
  <br><sub>Left: RViz, with the live co-flow speed readout. Right: AWSIM.</sub>
</p>

The shuttle localises against a prior lidar map of campus: 1.25 million points over roughly 840 m by
560 m, with a lanelet2 vector map on top for the drivable paths.

<p align="center">
  <img src="https://raw.githubusercontent.com/HTOLCH/HTOLCH/5e4e5747df043f97b250a7852fb23a3c4f10b065/media/campus_pointcloud_perspective.png" width="560" alt="Lidar pointcloud map of the UWA campus, perspective view, coloured by height">
</p>

---

<img align="right" width="260" src="https://raw.githubusercontent.com/HTOLCH/HTOLCH/bf5e42aedf46f11bd433d1e001cfa649a16013cb/media/pioneer.jpg" alt="Pioneer robot with lidar and onboard compute">

### Autonomous navigation and SLAM, simulation through to hardware

GPS-waypoint navigation with a tuned Kalman filter over IMU, lidar and GPS, plus 3D SLAM. Built in
Gazebo, then deployed on a Pioneer robot outdoors, which is where the assumptions that only hold in
simulation tend to surface. Perception ran on PyTorch: object detectors to find targets around the
course, and a vision-based policy mapping camera images straight to steering.

<br clear="all">

---

<img align="right" width="260" src="https://raw.githubusercontent.com/HTOLCH/HTOLCH/bf5e42aedf46f11bd433d1e001cfa649a16013cb/media/drone.jpg" alt="Custom-built 5 inch FPV quadcopter">

### FPV drones

I design, build, repair and fly custom FPV quadcopters. The one pictured is a 5 inch Armattan build.

Flight footage: **[youtube.com/@hazfpv771](https://www.youtube.com/@hazfpv771)**

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

Previously: engineering internships in mining and energy, at First Mode on a hydrogen haul-truck
retrofit and at GPA Engineering on pipelines. I tutor Mobile Robots, and Risk, Reliability & Safety,
at UWA.

---

I completed my Master's in 2026, I am available now, and I am looking for graduate robotics and
autonomy roles in Perth.

Perth, WA &nbsp;·&nbsp; [LinkedIn](https://www.linkedin.com/in/harry-tolcher-b69a65267/) &nbsp;·&nbsp; [YouTube](https://www.youtube.com/@hazfpv771) &nbsp;·&nbsp; harrytolcher1@gmail.com

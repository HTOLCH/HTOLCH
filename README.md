## Stuff I've Done
---

### Crowd-matching velocity planning for Autoware

*Master's thesis · [Code and write-up](https://github.com/HTOLCH/autoware_crowd_matching_module)*

<img align="right" width="260" src="https://raw.githubusercontent.com/HTOLCH/HTOLCH/7fb555da2c3af0c52297c284b962678a9e97b3c8/media/nuway_shuttle_sq.jpg" alt="The nUWAy autonomous shuttle, an EasyMile EZ10, on the UWA campus">

Out of the box, Autoware places a 5 m stop margin in front of every pedestrian it detects, which
makes a shared campus path undriveable. I wrote a `behavior_velocity_planner` plugin that identifies
the pedestrians moving with the vehicle, estimates the speed of the crowd, and smoothly matches it,
with proximity-based attenuation underneath so closing on the crowd never comes at the cost of
clearance.

To evaluate it I built a pedestrian simulation environment in AWSIM, with the crowd driven by a
Social Force Model that also served as the benchmark baseline. Across a sweep of pedestrian densities
the planner removed stop events entirely and held mean time-to-collision above 2.3 s. I also brought
the full Autoware stack up on the shuttle's own hardware, integrating it from a large and sparsely
documented codebase, and built the lidar perception that tracks pedestrians around the vehicle. The
planner was validated in simulation; the stack deployment ran on the vehicle.

<br clear="all">

<p align="center">
  <sub>Left: RViz, with the live co-flow speed readout. Right: AWSIM.</sub>
  <br>
  <img src="https://raw.githubusercontent.com/HTOLCH/autoware_crowd_matching_module/3a5c5a85b04ad23f0823731d918c1b4ec0605e81/docs/media/demo.gif" width="540" alt="Crowd-matching velocity planning in AWSIM simulation">
</p>

The planner localises against a prior lidar map of the campus: 1.25 million points over roughly 840
by 560 m, with a lanelet2 vector map for the drivable paths.

<p align="center">
  <img src="https://raw.githubusercontent.com/HTOLCH/HTOLCH/5e4e5747df043f97b250a7852fb23a3c4f10b065/media/campus_pointcloud_perspective.png" width="540" alt="Lidar pointcloud map of the UWA campus, coloured by height">
</p>

---

### Autonomous navigation and SLAM

*Sim-to-real on a mobile robot*

<img align="right" width="260" src="https://raw.githubusercontent.com/HTOLCH/HTOLCH/bf5e42aedf46f11bd433d1e001cfa649a16013cb/media/pioneer.jpg" alt="Pioneer robot with lidar and onboard compute">

GPS-waypoint navigation with a tuned Kalman filter fusing IMU, lidar and GPS, alongside 3D SLAM.
Developed in Gazebo, then deployed on a Pioneer robot outdoors, where the assumptions that only hold
in simulation tend to surface. On the perception side I trained PyTorch object detectors and a
vision-based policy that mapped camera images directly to steering.

<br clear="all">

---

### FPV drones

<img align="right" width="260" src="https://raw.githubusercontent.com/HTOLCH/HTOLCH/bf5e42aedf46f11bd433d1e001cfa649a16013cb/media/drone.jpg" alt="Custom-built 5 inch FPV quadcopter">

I design, build, repair and fly custom FPV quadcopters. The one pictured is a 5 inch Armattan build.
It keeps me close to the hardware, and there's flight footage on
[YouTube](https://www.youtube.com/@hazfpv771).

<br clear="all">

---

### Technical

- **Languages:** C++, Python
- **Robotics:** ROS 2, Autoware, motion and velocity planning, SLAM, state estimation and sensor fusion (Kalman)
- **Perception:** Lidar tracking and object detection, PyTorch, OpenCV, YOLO
- **Simulation:** AWSIM / Unity, Gazebo, sim-to-real testing
- **Mechanical:** SolidWorks, Siemens NX, MATLAB/Simulink, vehicle dynamics, BOM ownership
- **Electronics:** Soldering, flight-controller tuning, Raspberry Pi, motor characterisation, sensor integration
- **Tooling:** Linux, Git, Docker

Previously: engineering internships in mining and energy, at First Mode (hydrogen haul-truck
retrofit) and GPA Engineering (pipelines). I tutor Mobile Robots and Risk, Reliability & Safety at
UWA.

---

Perth, WA &nbsp;·&nbsp; [LinkedIn](https://www.linkedin.com/in/harry-tolcher-b69a65267/) &nbsp;·&nbsp; [YouTube](https://www.youtube.com/@hazfpv771) &nbsp;·&nbsp; harrytolcher1@gmail.com

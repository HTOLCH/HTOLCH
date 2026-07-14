## Harry Tolcher

Robotics and autonomy software engineer in Perth, Western Australia. C++ and Python, mostly on
ROS 2. I work on the part of the stack where planning and perception have to survive contact with
real hardware.

Master of Professional Engineering (Mechanical), UWA.

---

### Crowd-matching velocity planning for Autoware

*Master's thesis.* **[Code, results and full write-up](https://github.com/HTOLCH/autoware_crowd_matching_module)**

<img align="right" width="260" src="https://raw.githubusercontent.com/HTOLCH/HTOLCH/c55ca539e05c5aed611e9554a42e448b9bbfe12b/media/nuway_shuttle.jpg" alt="The nUWAy autonomous shuttle, an EasyMile EZ10, on the UWA campus">

The vehicle is nUWAy, an EasyMile EZ10 that runs on shared footpaths at UWA.

Stock Autoware places a 5 m stop margin in front of every pedestrian it detects. On a shared campus
footpath the shuttle stops continuously and never completes a route.

I wrote a `behavior_velocity_planner` plugin that identifies co-flow pedestrians, the ones moving in
the same direction as the vehicle, estimates the mean speed of the crowd, and smoothly converges the
shuttle onto it. Proximity-based velocity attenuation runs underneath, targeting zero speed at a
configurable minimum clearance, so matching the crowd never comes at the cost of clearance. I
implemented a classical Social Force Model (Helbing & Molnar, 1995) as the baseline to measure it
against.

Validated in AWSIM across a sweep of pedestrian densities, benchmarked against the baseline and a
range of planner and controller configurations. The setup I settled on removed stop events entirely
and held mean time-to-collision above 2.3 s. Marked 87.

<br clear="all">

<p align="center">
  <img src="https://raw.githubusercontent.com/HTOLCH/autoware_crowd_matching_module/3a5c5a85b04ad23f0823731d918c1b4ec0605e81/docs/media/demo.gif" width="560" alt="Crowd-matching velocity planning in AWSIM simulation">
  <br><sub>Left: RViz, with the live co-flow speed readout. Right: AWSIM.</sub>
</p>

Two other parts of the same project:

- A custom lidar perception engine that detects and tracks pedestrians around the vehicle in real
  time, GPU-accelerated with hand-written CUDA kernels to keep pace with the sensor rate.
- Bringing the full Autoware stack up on the nUWAy shuttle's own hardware, integrated from a large
  and sparsely documented codebase, with a safety fallback layer behind it.

To be precise about scope: the planner was validated in simulation. The stack deployment was on the
vehicle.

<img align="right" width="230" src="https://raw.githubusercontent.com/HTOLCH/HTOLCH/5e4e5747df043f97b250a7852fb23a3c4f10b065/media/campus_pointcloud.png" alt="Lidar pointcloud map of the UWA campus, top down, coloured by height">

**The map it localises against**

The prior lidar map of the UWA campus: 1.25 million points over roughly 840 m by 560 m, coloured by
height. Buildings, footpaths and tree canopies all fall out of it. A lanelet2 vector map sits on top
of this for the drivable paths and lane geometry.

<br clear="all">

---

<img align="right" width="260" src="https://raw.githubusercontent.com/HTOLCH/HTOLCH/bf5e42aedf46f11bd433d1e001cfa649a16013cb/media/pioneer.jpg" alt="Pioneer robot with lidar and onboard compute">

### Autonomous navigation and SLAM, simulation through to hardware

GPS-waypoint navigation with a tuned Kalman filter fusing IMU, lidar and GPS, alongside 3D SLAM.
Developed in Gazebo, then deployed and validated on a Pioneer robot outdoors, which is where the
assumptions that only hold in simulation tend to surface.

The perception side ran on PyTorch: object detectors to locate targets around the course, where I
chose YOLO over a custom model for inference speed, and a vision-based driving policy mapping camera
images directly to steering.

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
**Robotics** ROS 2, Autoware, motion and velocity planning, SLAM, state estimation and sensor fusion (Kalman), coordinate transforms
**Perception** Lidar tracking and object detection, CUDA, PyTorch, OpenCV, YOLO
**Simulation** AWSIM / Unity, Gazebo, sim-to-real testing
**Tooling** Linux, Git, Docker

Previously: engineering internships in mining and energy, at First Mode on a hydrogen haul-truck
retrofit and at GPA Engineering on pipelines. I tutor Mobile Robots, and Risk, Reliability & Safety,
at UWA.

---

I completed my Master's in 2026 and am looking for graduate robotics and autonomy roles in Perth.

Perth, WA &nbsp;·&nbsp; [LinkedIn](https://www.linkedin.com/in/harry-tolcher-b69a65267/) &nbsp;·&nbsp; [YouTube](https://www.youtube.com/@hazfpv771) &nbsp;·&nbsp; harrytolcher1@gmail.com

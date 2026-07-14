## Harry Tolcher

Robotics software engineer in Perth, Western Australia. I like building cool systems and getting
stuck into tough problems, mostly in C++ and Python.

Most of what I enjoy sits where the software meets the hardware: motion planning, perception, and
working out why the thing that ran perfectly in the sim is now doing something unexpected on the
robot. Master of Professional Engineering (Mechanical) at UWA, and a fair few personal projects that
got out of hand.

---

### Things I've built

**Crowd-matching velocity planning for Autoware** *(Master's thesis)*

Out of the box, Autoware slams on the brakes 5 m in front of every pedestrian it sees. Put that on a
busy campus footpath and the shuttle just stands there, forever. So I wrote a
`behavior_velocity_planner` plugin that spots the pedestrians walking the same way as the bus, works
out how fast the crowd is actually moving, and matches their speed instead of stopping dead.

The tricky part was doing that without ever letting it get too close to anyone. I settled it with an
8-way comparison of planners and controllers in AWSIM.

<p align="center">
  <img src="https://raw.githubusercontent.com/HTOLCH/autoware_crowd_matching_module/3a5c5a85b04ad23f0823731d918c1b4ec0605e81/docs/media/demo.gif" width="700" alt="Crowd-matching velocity planning in AWSIM simulation">
</p>

**[Code, results and the full write-up](https://github.com/HTOLCH/autoware_crowd_matching_module)**

I also got the full Autoware stack up and running on the actual nUWAy shuttle hardware, which was a
completely different flavour of pain to the simulation work.

---

<img align="right" width="300" src="https://raw.githubusercontent.com/HTOLCH/HTOLCH/main/media/pioneer.jpg" alt="Pioneer robot with lidar and onboard compute">

**Autonomous navigation and SLAM, sim to real**

GPS-waypoint navigation with a tuned Kalman filter fusing IMU, lidar and GPS, plus 3D SLAM. Built in
Gazebo first, then let loose on this thing outdoors. I also trained a few PyTorch models along the
way: object detectors to find letters around the course, and a vision-based driving policy that took
camera images straight to steering.

Watching it drive itself around outside never got old.

<br clear="all">

---

<img align="right" width="300" src="https://raw.githubusercontent.com/HTOLCH/HTOLCH/main/media/drone.jpg" alt="Custom-built 5 inch FPV quadcopter">

**FPV drones**

I build and fly custom FPV quads, and put the footage up on
**[youtube.com/@hazfpv771](https://www.youtube.com/@hazfpv771)**.

There is no grand reason for this one. It is just good fun.

<br clear="all">

---

### Stuff I work with

**Languages** C++, Python
**Robotics** ROS 2, Autoware, SLAM, motion and velocity planning, state estimation, sensor fusion (Kalman)
**Perception** Lidar tracking, object detection, CUDA, PyTorch, OpenCV, YOLO
**Simulation** AWSIM / Unity, Gazebo, sim-to-real testing
**Tooling** Linux, Git, Docker

Before the robotics I did engineering internships in mining and energy, at First Mode on a hydrogen
haul-truck retrofit and at GPA Engineering on pipelines. I also tutor Mobile Robots and Risk,
Reliability & Safety at UWA.

---

Perth, WA &nbsp;·&nbsp; [LinkedIn](https://www.linkedin.com/in/harry-tolcher-b69a65267/) &nbsp;·&nbsp; [YouTube](https://www.youtube.com/@hazfpv771) &nbsp;·&nbsp; harrytolcher1@gmail.com

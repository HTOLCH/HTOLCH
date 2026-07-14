## Harry Tolcher

Robotics software engineer in Perth, Western Australia. I like building cool systems and getting
stuck into tough problems, mostly in C++ and Python.

Most of what I enjoy sits where the software meets the hardware: motion planning, perception, and
working out why the thing that ran perfectly in the sim is now doing something stupid on the robot.
Master of Professional Engineering (Mechanical) at UWA, and a fair few personal projects that got
out of hand.

---

### Things I've built

**🚌 Crowd-matching velocity planning for Autoware** *(Master's thesis)*

Out of the box, Autoware slams on the brakes 5 m in front of every pedestrian it sees. Put that on a
busy campus footpath and the shuttle just stands there, forever. So I wrote a
`behavior_velocity_planner` plugin that spots the pedestrians walking the same way as the bus, works
out how fast the crowd is actually moving, and matches their speed instead of stopping dead.

The tricky part was doing that without ever letting it get too close to anyone. I settled it with an
8-way comparison of planners and controllers in AWSIM.

<p align="center">
  <img src="https://raw.githubusercontent.com/HTOLCH/autoware_crowd_matching_module/3a5c5a85b04ad23f0823731d918c1b4ec0605e81/docs/media/demo.gif" width="820" alt="Crowd-matching velocity planning in AWSIM simulation">
</p>

**[→ Code, results and the full write-up](https://github.com/HTOLCH/autoware_crowd_matching_module)**

I also got the full Autoware stack up and running on the actual nUWAy shuttle hardware, which was a
completely different flavour of pain to the simulation work.

**🤖 Autonomous navigation and SLAM, sim to real**

GPS-waypoint navigation with a tuned Kalman filter fusing IMU, lidar and GPS, plus 3D SLAM, built in
Gazebo and then let loose on a physical Pioneer robot outdoors. Also trained a few PyTorch models
along the way: object detectors to find letters around the course, and a vision-based driving policy
that took camera images straight to steering.

**🚁 FPV drones**

I build and fly custom FPV quads. This is where most of my "why did that break" education has come
from, and it is the reason I am comfortable with a soldering iron and a flight controller as well as
a compiler.

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

📍 Perth, WA · [LinkedIn](https://www.linkedin.com/in/harry-tolcher-b69a65267/) · harrytolcher1@gmail.com

## Harry Tolcher

Robotics software engineer in Perth, Western Australia. I write autonomy software in C++ and Python
that runs on real machines, not just in simulation.

Master of Professional Engineering (Mechanical), UWA. My thesis put a pedestrian-aware motion
planner onto an autonomous campus shuttle running the Autoware self-driving stack.

---

### Crowd-Matching Velocity Planning for Autoware

<p align="center">
  <img src="https://raw.githubusercontent.com/HTOLCH/autoware_crowd_matching_module/main/docs/media/demo.gif" width="620" alt="Crowd-matching velocity planning in AWSIM simulation">
</p>

Stock Autoware places a 5 m stop margin in front of every pedestrian it detects. On a shared campus
path, that means the shuttle stops constantly and never gets anywhere. I wrote a
`behavior_velocity_planner` plugin that detects co-flow pedestrians, computes their mean speed, and
smoothly matches it instead of stopping dead.

Validated across an 8-way comparative study in AWSIM, then deployed on the physical shuttle.

**[→ Code, results and full write-up](https://github.com/HTOLCH/autoware_crowd_matching_module)**

---

### What I work with

**Languages** C++, Python
**Robotics** ROS 2, Autoware, SLAM, motion and velocity planning, state estimation, sensor fusion (Kalman)
**Perception** Lidar tracking, object detection, CUDA, PyTorch, OpenCV, YOLO
**Simulation** AWSIM / Unity, Gazebo, sim-to-real testing
**Tooling** Linux, Git, Docker

Also: mining and energy engineering internships (First Mode, GPA Engineering), tutor for Mobile
Robots and for Risk, Reliability & Safety at UWA, and I build custom FPV drones.

---

📍 Perth, WA · [LinkedIn](https://www.linkedin.com/in/harry-tolcher-b69a65267/) · harrytolcher1@gmail.com

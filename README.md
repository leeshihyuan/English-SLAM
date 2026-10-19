Simultaneous Localization and Mapping（SLAM）TextBook PDF Part 1

How to build a vision-based navigation and localization drone,  

Editor: Lee Shihyuan (李世淵) LINE OA @prof



![Simultaneous Localization and Mapping（SLAM）](https://github.com/leeshihyuan/English-SLAM/blob/main/SLAM-Simultaneous-Localization-and-Mapping_Cover-Bald-Eagle.png "Simultaneous Localization and Mapping（SLAM）")


# Simultaneous Localization and Mapping (SLAM)

### A Taiwan-Authored University Textbook — Complete Edition, Chapters 1–34

|  |  |
| --- | --- |
| **Editor** | Lee Shihyuan (李世淵) · LINE OA @prof |
| **Assistants** | Aaron Lee, Anne Lee |
| **Course setting** | University Intelligent Robotics Program ／ High School AI and Robotics Club Course |
| **Extent** | 9 parts · 34 chapters · 976 pages |
| **Source file** | `SLAM_Complete_Edition_Ch1-34.docx` |

---

## About the Book

This book takes a reader who knows nothing of the subject from *what problem SLAM
solves* all the way to *I have built one with my own hands*. It begins with the
chicken-and-egg problem — a robot cannot localize without a map, and cannot map
without a pose — and ends thirty-four chapters later with a robot that accepts a
sentence of plain language, reasons about where to look, drives there, verifies
what it did, and reports back.

Three commitments run through every chapter.

**The figures are measurements, not decorations.** Every experimental figure in
this book was computed, not drawn to illustrate a point already decided: the
scan-registration kernel really is implemented three times and timed; the
sim-to-real gap really is closed by fitting a joint model to swept-frequency
data; the semantic search really is run six hundred times over randomly placed
objects. Where a measurement disagreed with the expected number, the text was
changed to follow the measurement.

**Limits come before methods.** Each sensor is introduced together with what it
cannot do, each algorithm together with how it fails, each platform together
with the resources it does not have. The thread running through the whole book
is that *only by understanding a limit can a limit be broken*.

**Each chapter is built the same way.** A chapter opens with *Where This Chapter
Sits in the Book* and a link map, then *Learning Objectives*, *Core Concepts*
(the body), worked *Cases* drawn from things that really go wrong,
*Implementation Activities*, *Discussion Questions*, an *Extended Challenge* at
university level, *Further Reading*, a *Summary*, and *Carrying Forward* — the
bridge to the next chapter. A bilingual glossary closes every chapter, with the
Chinese term kept beside the English one.

---

## How to Read It

| Reader | Suggested path |
| --- | --- |
| **University course, one semester** | Parts I–IV in full, then one of Part V (3D LiDAR) or Part VI (vision) as the technical core, closing with Part VIII for the implementation. |
| **University course, two semesters** | Parts I–IV, then V–VII, then VIII–IX; Chapter 31 supplies the marking rubric for the term project. |
| **High school club** | Chapters 1, 3, 4, 7–9, 13, 16, 20, 24, 28–29, and the first stage of each implementation activity. |
| **Self-study with hardware** | Part VIII first for the toolchain, then back to whichever of Parts IV–VII matches the sensor on the bench. |
| **Reader interested in AI robotics** | Part IX reads on its own, provided Chapters 10–13 are to hand. |

---

## The Nine Parts at a Glance

| Part | Title | Chapters | Pages | What it settles |
| --- | --- | --- | --- | --- |
| **I** | Introduction to SLAM and Autonomous Navigation | 1–3 | 4–80 | What the problem is, how the world teaches it, and where SLAM sits in a navigation system |
| **II** | Sensors for Localization and Navigation | 4–9 | 81–236 | What each sensor can answer, and under what conditions it lies |
| **III** | Mathematical Foundations of SLAM | 10–12 | 237–313 | One frame for every sensor, probability for every measurement, optimization over the whole history |
| **IV** | 2D SLAM and the Cleaning Robot | 13–16 | 314–420 | The first complete systems — and the same technology inside a product you can buy |
| **V** | 3D LiDAR SLAM and Autonomous Inspection | 17–19 | 421–508 | Out of the plane and into a site that must run every day for a year |
| **VI** | Visual SLAM and the Vision-Navigated Robot | 20–24 | 509–661 | From a pixel to a trajectory, and from a trajectory to an action |
| **VII** | Micro Robots, Drones and Edge AI SLAM | 25–27 | 662–754 | What happens when power, weight, speed and a single platform all run out |
| **VIII** | Implementation in ROS ／ Python ／ C++ | 28–31 | 755–888 | Making it actually run, and proving with numbers that it did |
| **IX** | AI, VLMs and Semantic Navigation SLAM | 32–34 | 889–976 | Meaning, skill and purpose — and the summing-up of the whole book |

---

## Contents

### Part I　Introduction to SLAM and Autonomous Navigation
*Chapters 1–3 · pages 4–80*

Part I settles three things before any mathematics appears: what problem SLAM
actually solves, how the subject is taught at the universities that lead it, and
why SLAM is never an end in itself but one link in a navigation system.

| Ch | Title | Page | In one line |
| --- | --- | --- | --- |
| 1 | What Is SLAM? | 4 | The chicken-and-egg problem: no map without a pose, no pose without a map |
| 2 | SLAM Courses at Leading Universities | 32 | How the subject is taught worldwide — and where this book's own structure came from |
| 3 | Robot Navigation Systems | 55 | Perception, localization, planning, control: the stack SLAM lives inside |

---

### Part II　Sensors for Localization and Navigation
*Chapters 4–9 · pages 81–236*

Part II takes the sensors one at a time and asks of each the same two questions:
what can it answer, and when does it quietly give a wrong answer? It moves from
absolute position (indoors, then outdoors), to absolute heading, to the
proprioceptive sensors that feel only themselves, and finally to the
exteroceptive sensors that measure the world.

| Ch | Title | Page | In one line |
| --- | --- | --- | --- |
| 4 | Indoor Positioning Technologies | 81 | Absolute position without a sky view: UWB, Wi-Fi, BLE and markers, and the accuracy each really buys |
| 5 | Radio and Satellite Navigation | 107 | GNSS and RTK outdoors — and what multipath and an urban canyon do to them |
| 6 | Geomagnetic Navigation and the Compass | 132 | Absolute heading from the magnetic field: slow, fragile, and still indispensable |
| 7 | IMU Inertial Navigation | 157 | Extremely fast and immune to disturbance, and wrong the instant you integrate it |
| 8 | An Introduction to LiDAR | 186 | Geometry measured directly — with glass, mirrors and specular returns as the failure modes |
| 9 | Cameras and Visual Navigation Sensors | 211 | No distance at all, and yet colour, texture, text and semantics |

---

### Part III　Mathematical Foundations of SLAM
*Chapters 10–12 · pages 237–313*

Every sensor in Part II speaks its own language. Part III supplies the three
tools that let them be spoken together: one coordinate frame, one calculus of
uncertainty, and one way of optimizing over everything that has been seen so
far rather than only the present instant.

| Ch | Title | Page | In one line |
| --- | --- | --- | --- |
| 10 | Coordinate Systems and Rigid-Body Motion | 237 | Rotations, transforms and the TF tree — the sentence every sensor must be translated into |
| 11 | Probability, Noise, and State Estimation | 261 | The Bayes filter and its three practical forms: Kalman, extended Kalman, particle |
| 12 | Optimization and Graph-Based SLAM | 288 | Keeping the history instead of discarding it: factor graphs, Gauss-Newton, loop closure |

---

### Part IV　2D SLAM and the Cleaning Robot
*Chapters 13–16 · pages 314–420*

Part IV assembles the tools of Part III into systems that actually run. It
builds a map with a known pose, then removes that assumption, then meets the
two classical answers — a particle filter and a pose graph — and finally finds
the whole of it inside a product on a shop shelf.

| Ch | Title | Page | In one line |
| --- | --- | --- | --- |
| 13 | Building a 2D Map | 314 | Occupancy grids, ray casting and log-odds: free, occupied, unknown |
| 14 | Gmapping: Particle Filter SLAM | 339 | Removing the known-pose assumption with a Rao-Blackwellized particle filter |
| 15 | Cartographer: Google's 2D ／ 3D SLAM | 364 | Submaps and branch-and-bound loop closure — the graph-optimization answer |
| 16 | SLAM in the Cleaning Robot | 392 | Sixteen chapters of technology inside a product: coverage planning and the rate of repetition |

---

### Part V　3D LiDAR SLAM and Autonomous Inspection
*Chapters 17–19 · pages 421–508*

Part V lifts everything out of the plane. More changes than a z coordinate: the
map grows by orders of magnitude, registration must be made cheap, a sweep is no
longer an instant, and a system that works in a demonstration must still work on
the three hundredth day.

| Ch | Title | Page | In one line |
| --- | --- | --- | --- |
| 17 | 3D Point Clouds and LiDAR Mapping | 421 | Downsampling, ICP and NDT: making a cloud of tens of thousands of points tractable |
| 18 | LOAM and LiDAR Odometry | 451 | Features instead of every point, and compensating the motion that happens during a sweep |
| 19 | Autonomous Inspection Robots and Field Practice | 480 | A year of daily running: map maintenance, repeatability, and what the site does to the robot |

---

### Part VI　Visual SLAM and the Vision-Navigated Robot
*Chapters 20–24 · pages 509–661*

Part VI changes the sensor but not the line of thought. It goes from a pixel to
a correspondence, from a correspondence to a camera motion, from a motion to a
complete system, and finally from a trajectory to an action the robot performs
with its own body.

| Ch | Title | Page | In one line |
| --- | --- | --- | --- |
| 20 | An Introduction to Visual SLAM | 509 | Features and descriptors: finding the same thing in two pictures |
| 21 | Epipolar Geometry and Camera Motion Estimation | 539 | Essential and fundamental matrices, PnP, triangulation — and where scale goes missing |
| 22 | ORB-SLAM2 in Theory and in Practice | 570 | Tracking, local mapping and loop closing assembled into a system that runs |
| 23 | ORB-SLAM3 and Visual-Inertial SLAM | 601 | The IMU restores scale; Atlas survives the loss of tracking |
| 24 | The Vision-Navigated Robot | 630 | Knowing where you are is not the point: markers, visual servoing, and acting on the estimate |

---

### Part VII　Micro Robots, Drones and Edge AI SLAM
*Chapters 25–27 · pages 662–754*

Part VII removes the premise the earlier parts never state aloud — that there is
computing power, battery and time to spare. It shrinks the platform, then makes
it fly, and then, having found the limits of any one machine, puts several of
them together.

| Ch | Title | Page | In one line |
| --- | --- | --- | --- |
| 25 | NanoSLAM and Low-Power SLAM | 662 | SLAM in a few hundred milliwatts: hardware and algorithm designed together |
| 26 | Drone SLAM and Visual-Inertial Navigation | 693 | Speed smears the corners and leaves no time to recover — so the system degrades by degrees |
| 27 | Multi-Robot SLAM and Cloud ／ Edge Collaboration | 725 | Map merging, bandwidth, robust back-ends, and what a team buys over a single robot |

---

### Part VIII　Implementation in ROS ／ Python ／ C++
*Chapters 28–31 · pages 755–888*

The first twenty-seven chapters are about how it ought to be done; Part VIII is
about making it run. It deals in the things that hold a project up for three
days — versions, empty topics, broken transform trees, a full disk — and it
insists that every claim be backed by a number the student measured.

| Ch | Title | Page | In one line |
| --- | --- | --- | --- |
| 28 | The SLAM Programming Environment | 755 | ROS 2, topics against services, and rosbag — with the real cost of each measured |
| 29 | Mapping with a 2D LiDAR Rover | 786 | The first end-to-end build: odometry calibration, TF, SLAM Toolbox, AMCL and Nav2 |
| 30 | RGB-D ／ Stereo Camera SLAM in Practice | 818 | Depth cameras, calibration, RTAB-Map — and LiDAR against vision on one site, four rooms |
| 31 | SLAM Projects and Their Assessment | 853 | A marking rubric, coverage and repetition metrics, the blind spots of an evaluation, and how much schedule slack a project really needs |

---

### Part IX　AI, VLMs and Semantic Navigation SLAM
*Chapters 32–34 · pages 889–976*

Part IX adds the three things a geometric map cannot supply: meaning, skill and
purpose. The last chapter also closes the book, taking one complete errand and
showing where each of the nine parts does its work.

| Ch | Title | Page | In one line |
| --- | --- | --- | --- |
| 32 | Semantic SLAM: Giving the Map a Meaning | 889 | The four levels of a semantic map, keeping people out of it, and turning meaning into navigation cost |
| 33 | Training in Simulation and Sim-to-Real | 912 | Parallel simulation, synthetic data, system identification against domain randomization, and deployment at the edge |
| 34 | VLMs, Language Navigation and Embodied Intelligence | 945 | One sentence into a goal: common-sense priors, RAG, a layered architecture, verification — and the summing-up of all thirty-four chapters |

---

## The Close of the Book

The last section of Chapter 34 takes a single service errand — *go to the
intelligent robotics classroom on the third floor, check the equipment in the
charging area, and report anything amiss* — and walks it through all nine
parts: the ideas of Part I, the sensors of Part II, the mathematics of Part III,
the SLAM systems of Parts IV to VI, the edge computing of Part VII, the tooling
of Part VIII, and the semantics, simulation and language of Part IX. Not one of
the nine can be spared. Without the geometric layer the robot hits a wall;
without the semantic layer it does not understand the instruction; without
training in simulation it never learns to move; without the toolchain nothing
runs at all.

That is the message the book carries from its first page to its last: SLAM is
not a single technique but a body of knowledge whose parts hold one another up.

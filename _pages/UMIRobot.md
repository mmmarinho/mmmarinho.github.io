---
layout: archive
title: "UMIRobot"
permalink: /UMIRobot/
author_profile: true
---

{% include base_path %}

The UMIRobot is a open {hardware, software} (5+1) robotic platform developed for online and hybrid learning courses.
The (under)graduate level students are divided into groups and have to design a gripper and a master control.

Detailed information is available in the [ArXiv preprint](https://arxiv.org/abs/2301.06668).

<img style='border:1px solid #000000' src="/images/umirobot_raytrace_front_withtext.png" width="250" height="200"> <img style='border:1px solid #000000' src="/images/umirobot_raytrace_up_withtext.png" width="250" height="200">
  
<hr/>

## Featured video: Japan <-> Bangladesh Teleoperation

An intercontinental teleoperation experiment between Japan and Bangladesh.
Using the UMIRobot and parts designed in this class.

[![IMAGE ALT TEXT](http://img.youtube.com/vi/Y_5amab3kMQ/0.jpg)](http://www.youtube.com/watch?v=Y_5amab3kMQ "Video Title")

<hr/>

## Past teleoperation challenge winners by category

|Year/Semester|Best gripper|Best master|Smoothest teleoperation|Best presentation|
|---|---|---|---|---|
|2022/Spring|Max-Mini Rex|Max-Mini Rex|Max-Mini Rex|Curious Lionhead|
|2021/Autumn|Inteligent Calicos|Inteligent Calicos|Inteligent Calicos|Curious Chaussies|
|2021/Spring|Unparalleled Shibas|Beady Beagles|Unparalleled Shibas|Unparalleled Shibas|

### 2022/Spring Videos

#### Max-Mini Rex

[![IMAGE ALT TEXT](http://img.youtube.com/vi/T65DRtAJ47Y/0.jpg)](http://www.youtube.com/watch?v=T65DRtAJ47Y "Video Title")

#### Curious Lionhead

[![IMAGE ALT TEXT](http://img.youtube.com/vi/o1naGEtkIeQ/0.jpg)](http://www.youtube.com/watch?v=o1naGEtkIeQ "Video Title")

### 2021/Autumn Videos

#### Inteligent Calicos 

[![IMAGE ALT TEXT](http://img.youtube.com/vi/CfaNs1w4wMY/0.jpg)](http://www.youtube.com/watch?v=CfaNs1w4wMY "Video Title")

#### Robotic Tabbys 

[![IMAGE ALT TEXT](http://img.youtube.com/vi/zix5uXahhFg/0.jpg)](http://www.youtube.com/watch?v=zix5uXahhFg "Video Title")

#### Curious Chaussies 

[![IMAGE ALT TEXT](http://img.youtube.com/vi/dfVOAAa_DoQ/0.jpg)](http://www.youtube.com/watch?v=dfVOAAa_DoQ "Video Title")

<hr/>

## Mechanical 

The 3D-printer-friendly files are shared over at [Thingiverse](https://www.thingiverse.com/thing:4797804).

<hr/>

## Software

There are two main software components related to the UMIRobot. 

### (A) [umirobot-arduino](https://github.com/mmmarinho/umirobot-arduino)

The Arduino example sketch must be uploaded to the Arduino connected to your UMIRobot.
1. Install the UMIRobot Arduino library [[Instructions]](https://www.ardu-badge.com/UMIRobot).
2. Upload the UMIRobot sketch to your Arduino.

### (B) [umirobot-py](https://github.com/mmmarinho/umirobot-py)

You can interact with your UMIRobot through your computer using a python-based program.
In a computer with a `Python >= 3.8` enviroment:
1. Create a `venv`
2. Install the `umirobot` package
3. Run the module with `python3 -m umirobot`
4. Rejoice

<hr/>

## Electronic

<a href="/images/umirobot_pcb_schematics.pdf" class="box">
<img style='border:1px solid #000000' src="/images/umirobot_pcb_schematics.png" width="480" height="300">
</a>

<hr/>

## License

Mechanical files: [CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/).
<br />Software: [GPLv3](https://tldrlegal.com/license/gnu-general-public-license-v3-(gpl-3)).

Note: The copyright for the student's designs remain with them. 

---
layout: archive
title: "UMIRobot"
permalink: /UMIRobot/
author_profile: true
---

{% include base_path %}

The UMIRobot is a open {hardware, software} (5+1) robotic platform developed for online and hybrid learning courses.
The (under)graduate level students are divided into groups and have to design a gripper and a master control.

<img style='border:1px solid #000000' src="/images/umirobot_raytrace_front_withtext.png" width="400" height="300"> <img style='border:1px solid #000000' src="/images/umirobot_raytrace_up_withtext.png" width="400" height="300">
  
<hr/>

## License

Mechanical files: [CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/).
<br />Software: [GPLv3](https://tldrlegal.com/license/gnu-general-public-license-v3-(gpl-3)).

Note: The copyright for the student's designs remain with them. 

<hr/>

## Past teleoperation challenge winners by category

|Year/Semester|Best gripper|Best master|Smoothest teleoperation|Best presentation|
|---|---|---|---|---|
|2022/Spring|Max-Mini Rex|Max-Mini Rex|Max-Mini Rex|Curious Lionhead|
|2021/Autumn|Inteligent Calicos|Inteligent Calicos|Inteligent Calicos|Curious Chaussies|
|2021/Spring|Unparalleled Shibas|Beady Beagles|Unparalleled Shibas|Unparalleled Shibas|

### 2022/Spring Videos

|Max-Mini Rex|Curious Lionhead|
|---|---|
|<video src="https://filedn.com/l0UYPwn5UWvjkjpImQ8wWeV/tr_2022_S_max_mini_rex_480p.mp4" controls="controls" style="max-height: 200px;"></video>|<video src="https://filedn.com/l0UYPwn5UWvjkjpImQ8wWeV/tr_2022_S_curious_lionhead_480p.mp4" controls="controls" style="max-height: 200px;"></video>|

### 2021/Autumn Videos

|Inteligent Calicos|Robotic Tabbys|Curious Chaussies|
|---|---|---|
|{% include youtube.html id="CfaNs1w4wMY" %}|{% include youtube.html id="zix5uXahhFg" %}|{% include youtube.html id="dfVOAAa_DoQ" %}|

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

**Under construction**

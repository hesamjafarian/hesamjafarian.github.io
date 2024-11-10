---
layout: archive
title: "Projects"
permalink: /projects/
author_profile: true
redirect_from:
  - /resume
---

## Autonomous Cars

## Small Size Robots

### Overview
In the Small Size League (SSL), each team constructs autonomous cylindrical robots that play soccer with an orange golf ball. During the match, eight robots from each team work to score goals using swift passing maneuvers and intense dueling strategies. The robot system operates entirely autonomously, meaning no team member is allowed to control the robots directly. Instead, a central PC (typically a simple laptop) receives preprocessed camera data, runs the team's AI, and communicates with the robots via radio.

### The Playing Field
The playing field measures 9m x 12m and is covered with a carpet. All 22 robots are monitored by two USB cameras positioned above the field, connected to a centralized vision computer. Each robot's top plate features a standardized pattern known as the “Butterfly Pattern” (made of colored paper), clearly identifying its jersey number and team affiliation. The color in the center indicates team affiliation (blue vs. yellow team), while the butterfly design around it represents the jersey number. Additionally, the front two points are spaced further apart than the back ones, allowing the camera to determine the robot’s orientation.

![Playing Field](images/system.jpg)

### The Robots
Robot sizes are limited by rules to a diameter of 18 cm and a height of 15 cm, leading to similar appearances. However, the mechanical and electrical designs can vary significantly. Most systems are built with four omni-wheels and electromagnetic kicker devices for linear and chip kicks.

![Robot](path/to/robot_image.jpg)

### Referee
Currently, a human main referee is responsible for all decisions, supported by a second assistant referee and a RefBox operator. The RefBox is a dedicated computer used to input all decisions, which are then sent to the teams via network connection. Autonomous referee systems, known as Autorefs, have been developed to automate the game further and will see increased use in the league.

### Competing Teams
Both opposing teams receive information from the RefBox and Vision systems via a local network. From this point, it is the team's responsibility to process the input. Typically, the camera data is further analyzed to detect the geometrical placement of robots and the ball on the field. The team's AI then determines a strategy and sends its current decisions to the robots approximately 60 times per second to ensure smooth movements. During the game, no team member is allowed to touch the computer running the strategy. Changes can only be made during timeouts and halftime. One team member is allowed to communicate with the referee and exchange robots on the field.

![Competing Teams](path/to/competing_teams_image.jpg)



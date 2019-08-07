---
layout: single
classes: wide
title: "Create the RCRS Scenario"
permalink: /resources/Create_Scenario/
read_time: true
toc: false
---
The RoboCup Rescue Simulation (RCRS) requires a disaster scenario to be used in simulators. The scenarios include information of the map of the disaster zone, location of rescue teams and civilians, location of urban facilities (i.e., refuge, gas station, etc.) and location fire. The role of each urban facility or rescue team and the simulation interaction when a fire occurs can be found on [this page]({{site.url }}{{site.baseurl }}/resources/RCRS/) or in [the official manual of RCRS](https://roborescue.sourceforge.io/docs/rcrs-manual.pdf). Therefore, you can create the scenario of RCRS as follows:
 1. Build the map of the scenarios
 2. Build the configuration (i.e., location of the rescue team, civilians, fire, etc.) of the scenarios.  



## Build the map of the scenarios
In the RCRS, the simulator simulates the earthquake occurs in the city according to a specific disaster scenario. The city where the earthquake will occur can be selected from the [Open Street Map (OSM)](https://www.openstreetmap.org) because the RCRS has a program that converts maps on the OSM into maps to be used for simulation. You can refer [the official tutorial of RCRS](https://roborescue.sourceforge.io/docs/map_creation-tutorial.pdf) to see how to create the map using OSM.

Furthermore, you can use the example map of RCRS which used in the competition of the RoboCup Rescue Simulation League. In our Scenario Generator includes the example map used in the 2017 competition. If you want to download the example map, you can refer to [this page](https://github.com/roborescue/rcrs-server/tree/master/maps/gml). When you finish building the map or download the example map, you can see the `config` and `map` directory.

## Build the configuration of the scenario
In the scenario directory, you can see the `config` and `map` directory. 

First, in the `config` directory, you can change the parameter of scenarios. For example, in the `kernel.cfg`, you can change the number of `kernel.timesteps` to set the time step of the scenario. And there are many other parameters you can change, however, you don't need to change the other parameter if you want to use our scenario generator. To see the other parameter of the scenario, please refer to [the official RoboCup Rescue Simulation Page](https://rescuesim.robocup.org/). 

Second, in the `map` directory, you can see the `map.gml` and `scenario.xml` file. You should not touch the `map.gml` file and you can set the `scenario.xml` to change the number of the rescue team, civilians, facility and the location of the rescue team, civilians, facility. In this file, you should change `<scenario:refuge scenario:location="19490"/>`. The 

`scenario:${the rescue team or civilian or facuilty}$

 scenario:location="${the location of }$"`

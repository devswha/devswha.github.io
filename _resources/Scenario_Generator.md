---
layout: single
classes: wide
title: "Scenario Generator"
permalink: /resources/Scenario_Generator/
read_time: true
toc: false
---

We developed a scenario generator to train the machine running model. In deep learning with image processing, it takes a lot of image data to train the machine learning model. And it takes a lot of work to generate this amount of data by a human. Therefore, we have developed a scenario generator that automatically generates simulated image data. Our scenario generator run as follows: (1) Input the setting of scenario (i.e., the number of civilians and fires, location of the rescue team, etc.) and the number of scenarios to create; and (2) The generator automatically runs the scenario on RCRS; and (3) As the simulation runs, the generator automatically parses the screenshot image data and text data (i.e., the number of injured civilians, rescue team location, etc.)

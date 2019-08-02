---
layout: single
classes: wide
title: "Scenario Generator"
permalink: /resources/Scenario_Generator/
read_time: true
toc: false
---
In RCRS, there are civilians in the disaster zone random location. And as the disaster progresses, the building collapses or fires cause injured civilians. Therefore, we predict the location of hidden injured civilians in RCRS. And the civilians have information called Health Point (HP) that shows how much they are injured status. Due to the disaster situation in simulators, likes fires spread or buildings collapse, civilians' HP going to lower. We set the HP threshold which determines the civilians is injured or not. If one civilian' HP lower than this threshold, we determine this civilian is injured. In this study, we propose the "Hidden Injured Problem" problem whose goal is to find the location of this injured civilians. In this problem, we suppose the \textit{x} and \textit{y} are the coordinate of the map where the  \( 1 \leq x \leq X \)  and  \( 1 \leq y \leq Y \). And the location of civilians is chosen randomly, the location of the rescue team and initial fire start building in the simulation is fixed. In addition, each time step \textit{\textbf{t}} exists in the simulation, as time step increase, fires spread or building collapses become more severe, thus increasing the number of injured civilians. Accordingly, the rescue team moves and tracks the location of the injured people. Therefore, even if the initial location of civilians is random, the location of the occurrence of the injured civilian will have a constant pattern as the disaster scenario progresses.

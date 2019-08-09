---
layout: single
classes: wide
title: "Video based Machine Learning Model"
permalink: /resources/Video_ML/
read_time: true
toc: false
---
In predict the density of injured civilian in RCRS using video-based data, we train the machine learning model using simulation screenshot image sequence. We consider that all frames of video clip are used for training. Therefore, we choose nine frames randomly in images sequence of disaster scenario in RCRS to train the machine learning model and predict the density of the 10th frame which is the next frame of 9th of the nine frames. The machine learning model's inputs are simulated images created and filtered from Plug-in1 and extract images feature using CNN. Afterwards, the Long-short memory (LSTM) extract sequence image feature from CNN. And fully-connected layer output the number of injured people vectors in each grid cell. The different from image-based predictions is add LSTM layer to sequence learning on video.

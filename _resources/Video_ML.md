---
layout: single
classes: wide
title: "Video based Machine Learning Model"
permalink: /resources/Video_ML/
read_time: true
toc: false
---
In predict the density of injured civilian in RCRS using video-based data, we train the machine learning model using simulation screenshot image sequence. We consider that all frames of video clip are used for training. Therefore, we choose nine frames randomly in images sequence of disaster scenario in RCRS to train the machine learning model and predict the density of the 10th frame which is the next frame of 9th of the nine frames. The machine learning model's inputs are simulated images created and filtered from Plug-in1 and extract images feature using CNN. Afterwards, the Long-short memory (LSTM) extract sequence image feature from CNN. And fully-connected layer output the number of injured people vectors in each grid cell. The different from image-based predictions is add LSTM layer to sequence learning on video.


![Robocup Rescue Simulation]({{site.url }}{{site.baseurl }}/assets/images/Video_ML.png){: .align-center}


## 1. Software Pre-Requisites
- TensorFlow 1.12.0
- Keras 2.2.4


## 2. Download project from GitHub and decompress RCRS
```bash
$ git clone https://github.com/swhaKo/Video-based-ML-with-RCRS.git
```

## 2. Configuration
In this repository, there is configuration file called "config.txt". You can modify the number of civilians, the number of initial fire building and the number of data sets. Also you can modifiy the path where datasets are stored.  

### Directory data constant
DATASET_DIR: The path of data set directory  
TRAIN_GENERATED_MAP_DIR: The path of the source of simulation map data for training  
TRAIN_GENERATED_IMAGE_DIR: The path of the screenshot image of simulation map data for training  
TEST_GENERATED_MAP_DIR: The path of the source of simulation map data for testing  
TEST_GENERATED_IMAGE_DIR: The path of the screenshot image of simulation map data for testing  

## 4. Execute

Label the generated disaster scenarios data
```bash
$ python3 ScenarioLabel_train.py [Map Name]
$ python3 ScenarioLabel_test.py [Map Name]
```

```bash
$ python3 train_data_generator.py [Map Name]
$ python3 test_data_generator.py [Map Name]
```

## 6. Download Link
[Video-based Machine Learning Model with RCRS GitHub Page](https://github.com/swhaKo/Video-based-ML-with-RCRS)

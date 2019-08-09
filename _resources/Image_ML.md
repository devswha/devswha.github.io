---
layout: single
classes: wide
title: "Image based Machine Learning Model"
permalink: /resources/Image_ML/
read_time: true
toc: false
---
To predict the density of injured civilian in RCRS using image-based data, we train the machine learning model using simulation screenshot images. We consider that all frames of video clip in disaster situations are independent images. Therefore, we choose one frame randomly in images sequence of a disaster scenario in RCRS to train the machine learning model. The model's inputs are simulated images created from RCRS. And CNN extracts images features, fully-connected layer output the number of injured people vectors in each grid cell.

![Robocup Rescue Simulation]({{site.url }}{{site.baseurl }}/assets/images/Image_ML.png){: .align-center}

1. Label the data created Scenario Generator
2. Convert the data labeled in the first step to image data
3. Train the machine learning model with data converted in the second step. 


## 1. Software Pre-Requisites
- TensorFlow 1.12.0
- Keras 2.2.4


## 2. Download project from GitHub and decompress RCRS
```bash
$ git clone https://github.com/swhaKo/Image-based-ML-Model.git
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
[Image-based Machine Learning Model with RCRS GitHub Page](https://github.com/swhaKo/Image-based-ML-Model)

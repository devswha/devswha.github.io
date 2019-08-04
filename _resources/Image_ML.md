---
layout: single
classes: wide
title: "Image_based Machine Learning Model"
permalink: /resources/Image_ML/
read_time: true
toc: false
---
To predict the density of injured civilian in RCRS using image-based data, we train the machine learning model using simulation screenshot images. We consider that all frames of video clip in disaster situations are independent images. Therefore, we choose one frame randomly in images sequence of a disaster scenario in RCRS to train the machine learning model. The model's inputs are simulated images created from RCRS. And CNN extracts images features, fully-connected layer output the number of injured people vectors in each grid cell.

![Robocup Rescue Simulation]({{site.url }}{{site.baseurl }}/assets/images/Image_ML.png){: .align-center}

In this study, we research the method of enhancing the performance of the machine learning model to predict the number of injured civilians in RCRS. And we evaluate the prediction performance of the different machine learning model to find the best performance of the machine learning model. To enhance the performance of the machine learning model, first, we find the best CNN model to extract the images feature. Second, we expect to see better performance by applying the attention mechanism to best CNN model found in the first step. Finally, we apply our own data augmentation method to simulation data set for training machine learning model.

## 1. Software Pre-Requisites
- TensorFlow 1.14
- Keras 2.3.0

## 2. Download project from GitHub and decompress RCRS
```bash
$ git clone https://github.com/swhaKo/RCRS-deep-learning.git
$ cd RCRS-deep-learning/
$ unzip RCRS.zip
```

## 3. Configuration
In this repository, there is configuration file called "config.txt". You can modify the number of civilians, the number of initial fire building and the number of data sets. Also you can modifiy the path where datasets are stored.  

### Map data constant
NUM_OF_CIVILIANS: The number of civilians in the simulation map  
NUM_OF_FIRES: The number of initial fire buildings  
LIMIT_TIME_STEP: The start point of disaster scenario time step to save image dataset.  
LIMIT_CIVILIAN_HP: The treshold of civilians' HP point which determine civilian is injured or not

### Train and test data constant
TRAIN_START_MAP_NUM: The map data start number for training  
TRAIN_END_MAP_NUM: The map data end number for training  
TEST_START_MAP_NUM: The map data start number for testing  
TEST_END_MAP_NUM: The map data end number for testing  

### Directory data constant
DATASET_DIR: The path of data set directory  
TRAIN_GENERATED_MAP_DIR: The path of the source of simulation map data for training  
TRAIN_GENERATED_IMAGE_DIR: The path of the screenshot image of simulation map data for training  
TEST_GENERATED_MAP_DIR: The path of the source of simulation map data for testing  
TEST_GENERATED_IMAGE_DIR: The path of the screenshot image of simulation map data for testing  

## 4. Execute
```bash
$ python3 train_data_generator.py [Map Name]
$ python3 test_data_generator.py [Map Name]
```

## 5. Map List
- Kobe
- Joao

## 6. Download Link
[Robocup Rescue Simulation Scenario Generator GitHub Page](https://github.com/swhaKo/Scenario_Generator)

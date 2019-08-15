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

And our program train the machine learning model as follows:
1. Label the data created Scenario Generator
2. Convert the data labeled in the first step to image data
3. Train the machine learning model with data converted in the second step.
4. Test the machine learning model with machine learning model trained in the third step.


## 1. Software Pre-Requisites
- TensorFlow 1.12.0
- Keras 2.2.4


## 2. Download project from GitHub and decompress RCRS
```bash
$ git clone https://github.com/swhaKo/Image-based-ML-Model.git
```

## 2. Configuration
In this repository, there is configuration file called *config_image.txt*. You can modify the number of civilians, the number of initial fire building and the number of data sets. Also you can modifiy the path where datasets are stored.  

### Constant of label the data
LIMIT_TIME_STEP: The start point of disaster scenario time step to save image dataset.  
LIMIT_CIVILIAN_HP: The threshold of civilians' HP point which determine civilian is injured or not
LABEL_TRAIN_START_MAP_NUM: The map data start number for training to label
LABEL_TRAIN_END_MAP_NUM: The map data end number for training  to label
LABEL_TEST_START_MAP_NUM: The map data start number for testing to label
LABEL_TEST_END_MAP_NUM: The map data end number for testing to label
LABEL_DATASET_DIR: The path of scenario directory to label

### Constant to convert the data
CONVERT_TRAIN_START_MAP_NUM: The map data start number for training to convert
CONVERT_TRAIN_END_MAP_NUM: The map data end number for training to convert
CONVERT_TEST_START_MAP_NUM: The map data start number for testing to convert
CONVERT_TEST_END_MAP_NUM: The map data end number for testing to convert
CONVERT_DATASET_DIR: The path of scenario directory to convert

### Constant to train and test the ML model
MODEL_TRAIN_START_MAP_NUM: The map data start number for training
MODEL_TRAIN_END_MAP_NUM: The map data end number for training
MODEL_TEST_START_MAP_NUM: The map data start number for testing
MODEL_TEST_END_MAP_NUM: The map data end number for testing
MODEL_DATASET_DIR: The path of scenario directory to train and test
MODELS_DIR: The path of machine learning model to save
RESULTS_DIR: The path of result to save

## 3. Label the density of injured civilians to scenario
We use the machine learning model to predict the location of the injured. And predict the exact location of injured civilians requires considerable computational resources and complexity, so that we divide the simulation map into grid and predict the density of the injured people in each grid cell. This can significantly shorten computational resources, complexity and the time required for training. Furthermore, we expected that the accuracy of the prediction of the injured civilians location will also be increased.

![Robocup Rescue Simulation]({{site.url }}{{site.baseurl }}/assets/images/Label.png){: .align-center}

And our program can automatically label the scenario follow this commands:

```bash
$ python3 Labeler_train.py [Map name] [Row of grid] [Column of grid]
$ python3 Labeler_test.py [Map name] [Row of grid] [Column of grid]
```

## 4. Convert the scenario to image
To train the machine learning model, we convert the scenario data which labeded in the step three. Our program automatically convert the scenario data to images using as follows commands:

```bash
$ python3 Converter_train_image.py [Map name] [Row of grid] [Column of grid]
$ python3 Converter_test_image.py [Map Name] [Row of grid] [Column of grid]
```

## 5. Train the machine learning model to predict


```bash
$ python3 Model_train_image.py [Map name] [Row of grid] [Column of grid]
$ python3 Model_train_image.py [Map Name] [Row of grid] [Column of grid]
```

## 6. Download Link
[Image-based Machine Learning Model with RCRS GitHub Page](https://github.com/swhaKo/Image-based-ML-Model)

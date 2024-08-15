---
layout: single
classes: wide
title: "Feature Highlight Data Augmentation"
permalink: /projects/augmentation/
read_time: true
toc: false
---
In deep learning with image processing, the deep learning model train images according to the feature of images. And the accuracy of deep learning model is affected by whether the model trains the feature of images well. Therefore, this study proposes the data augmentation method to help the model training more about the feature of images within the images for predicting the results well. In RCRS, injured civilians are occurred by fire or collapse of a building. And the rescue teams patrol to find injured civilians.  


![Robocup Rescue Simulation]({{site.url }}{{site.baseurl }}/assets/images/RCRS/Augmentation.png){: .align-center}

  
We expect that the important image of features to predict the location of injured civilians is the location of the object which relates to the injured civilians such as the location of collapsed buildings, locations of fires and rescue teams. Therefore, we study the data augmentation method that highlighting the important location which is related to the result in the image. We expect that this augmentation method allows the machine learning model to focus more on the feature of images in the training process. Therefore, we resizing, cropping, and highlighting of simulation image data which contribute to the increase the efficiency of training and prediction accuracy of the deep learning model.
{: style="text-align: justify;"}

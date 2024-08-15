---
layout: single
classes: wide
title: "Attention Module"
permalink: /projects/attention/
read_time: true
toc: false
---
![Robocup Rescue Simulation]({{site.url }}{{site.baseurl }}/assets/images/RCRS/Attention.png){: .align-center}


Apart from the CNN model of depth, width, and cardinality factors, we investigate a different aspect of the CNN architecture design, attention. The significance of attention has been studied extensively in the previous literature. Our goal is to increase the focus image feature power of CNN by using attention mechanism: focusing on important features and suppressing unnecessary ones. [Hu et al.](http://openaccess.thecvf.com/content_cvpr_2018/html/Hu_Squeeze-and-Excitation_Networks_CVPR_2018_paper.html) propose the *Squeeze and excitation (SE)* module which use global average-pooled features to compute channel-wise attention. [Woo et al.](http://openaccess.thecvf.com/content_ECCV_2018/html/Sanghyun_Woo_Convolutional_Block_Attention_ECCV_2018_paper.html) propose *Convolutional Block Attention Module (CBAM)*, which use max-pooled features as well that is a simple yet effective attention module for feed-forward convolutional neural networks. Furthermore, we proposed the new attention module which called *Grid Convolutional Block Attention Module (GCBAM)*. This attention module divides the two-dimension image feature vector to certain grid size. And use max-pooled features as well that is a simple yet effective attention module for feed-forward convolutional neural networks.
{: style="text-align: justify;"}


[Squeeze and excitation github Page (Keras)](https://github.com/titu1994/keras-squeeze-excite-network)

[Convolutional Block Attention Module github Page (Keras)](https://github.com/kobiso/CBAM-keras)

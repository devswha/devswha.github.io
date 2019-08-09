---
layout: single
classes: wide
title: "Attention Module"
permalink: /resources/Attention/
read_time: true
toc: false
---

Apart from the CNN model of depth, width, and cardinality factors, we investigate a different aspect of the CNN architecture design, attention. The significance of attention has been studied extensively in the previous literature \cite{mnih2014recurrent,ba2014multiple,bahdanau2014neural,xu2015show,gregor2015draw,jaderberg2015spatial}. Our goal is to increase the focus image feature power of CNN by using attention mechanism: focusing on important features and suppressing unnecessary ones. Hu \textit{et al.}\cite{hu2018squeeze} propose the \textit{Squeeze and excitation (SE)} module which use global average-pooled features to compute channel-wise attention. Woo \textit{et al.}\cite{woo2018cbam} propose \textit{Convolutional Block Attention Module (CBAM)}, which use max-pooled features as well that is a simple yet effective attention module for feed-forward convolutional neural networks. Furthermore, we proposed the new attention module which called \textit{Grid Convolutional Block Attention Module (GCBAM)}. This attention module divides the two-dimension image feature vector to certain grid size. And use max-pooled features as well that is a simple yet effective attention module for feed-forward convolutional neural networks. In this study, we use SE, CBAM and GCBAM attention module to the model chosen by the previous experiment which performs well.

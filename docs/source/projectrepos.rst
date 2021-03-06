Software Repositories and Project Demos 
==========================================

Summary
--------
This page contains the software repositories that were generated during the project execution and were demonstrated at the various seminars.
The repositories provide example implementations of various Machine Learning topics tailored for use on single board computers and constrained hardware.



Seminar 1: Outlier detection on KDD Cup dataset
------------------------------------------------
The first seminar details an implementation of real time outlier detection on a Raspberry Pi 4 single board computer. The demo is based on the `kddcup99 <http://kdd.ics.uci.edu/databases/kddcup99/kddcup99.html>`_ dataset which contains 
metrics of TCP/IP network connections and the aim is to detect malicious connections and hacking attempts. To achieve this an Isolation Forest model from the `Scikit learn <https://scikit-learn.org/stable/>`_ library is trained and evaluated on this dataset. Furthermore, in the code it is demonstrated how the trained model can be converted to a generic format (`ONNX <https://onnx.ai/>`_) which is independent of the Machine learning framework and useable in multiple programming languages.    
The ONNX representation eliminates dependencies and allows to run inference on all sorts of hardware more easily. The repository containing this demo can be found `here  <https://github.com/WillemRaes/AISIBOCOseminar2020>`_ .

.. image:: ../images/workflowseminar1.png
  :width: 800
  :alt: Alternative text


Seminar 2: Image and video processing for object detection and classification 
---------------------------------------------------------------------------------
The second seminar is on the topic of real time image classification and object detection using a `Jetson Nano <https://developer.nvidia.com/embedded/jetson-nano-developer-kit>`_ single board computer.
An implementation of real-time image classification and object detection is demonstrated using `Tensorflow <https://www.tensorflow.org/>`_ as ML framework. In the first part of the seminar a resnet50v2 backbone for image classification pre-trained on the `Imagenet <https://www.image-net.org/>`_ dataset, is converted to the ONNX format and used in a real-time image classification pipeline which processes a video stream of a smartphone camera and can detect 1000 objects.

.. image:: ../images/workflowseminar2.png
  :width: 800
  :alt: Alternative text

.. image:: ../images/sem2consideredimplementations.png
  :width: 800
  :alt: Alternative text

In the second part of the seminar a Resnet Centernet model backbone, pre-trained on the `MSCOCO <https://www.tensorflow.org/hub>`_ dataset, is downloaded via the `Tensorflow Hub <https://www.tensorflow.org/hub>`_ utility and used in a real-time Object detection pipeline, again processing a camera stream of a smartphone.   

.. image:: ../images/sem2demoapp.png
  :width: 800
  :alt: Alternative text


The repository containing this demo can be found in the `seminar 2 <https://github.com/WillemRaes/AISIBOCOseminar2>`_ repository.
Lastly a demonstration on how to build and train an image segmentation model based on the `cityscapes <https://www.cityscapes-dataset.com/>`_ dataset is given and the code can be found in the same repository.


Seminar 3: Image segmentation and model optimization 
---------------------------------------------------------------------------------
The third seminar focuses on model optimizations for better performance on single board computers. During this seminar, 2 single board computers are considered for real-time image segmentation, namely the Jetson nano and Jetson TX2 developer kits from NVIDIA. The implementations in this seminar strongly leverage an exisiting repository of NVIDIA and can be found here: `Jetson inference <https://github.com/dusty-nv/jetson-inference>`_ . This repo contains ML inference examples for object detection and image segmentation use cases and is strongly optimized for NVIDIA hardware. Importantly, it also provides automated model optimization and parameter quantization via the `TensorRT <https://developer.nvidia.com/tensorrt>`_ engine.
In this seminar we demonstrate real-time image segmentation of car traffic and the environment in the city of Ghent based on a video of a trajectory through the city done by bicycle. More specifically, the difference in latency between local computing on a Jetson Nano and 'cloud' computing on the Jetson TX2 is demonstrated. 

.. image:: ../images/sem3trtworkflow.png
  :width: 800
  :alt: Alternative text

.. image:: ../images/sem3latencycomp.png
  :width: 800
  :alt: Alternative text

The code for this implementation can be found in the `seminar 3 <https://github.com/WillemRaes/AISIBOCOseminar3>`_ repository.


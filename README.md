# UW - Eau Clare - GAN Generated MRI Research
Contributors: Tanner Hall, Elena Bourget, Kayla Behnke

## Overview
This research is designed to implement and evaluate several different strategies of image generation for the creation of MRI brain scans and their use in training the accuracy of a convolutional neural networks that is used to detect if an image contains a tumor in it in order to assist medical professionals.

## Projects
The code developed for this research can be broken into several parts. Firstly, each of the GAN techniques are independant programs designed to be run independantly. Each of these contains slight variation but start and end with the same input parameters and returned results. The other code consists of convolutional neural networks. The first implementation is a visualization of accuracy and visualizes the results, while the second is the an ehhnaced implementation that measures more metrics and untilized k-fold cross validation. Each major component is listed below.

### DC GAN
Developed by: Tanner Hall


### Unrolled GAN
Developed by: Kayla Behnke


### W GAN
Developed by: Elena Bourget


### Convolutional Neural Network
#### Initial Implemention
Developed by: Tanner Hall, Kayla Behnke, and Elena Bourget

#### Modified Implementation
Developed by: Tanner Hall and Kayla Behnke


## Reports
An inital report presentation was created in spring 2023 for use at the National Conference on Undergraduate Research (NCUR) held at the University of Wisconsin - Eau Claire. A poster was showcased to outline the results of the research. The poster is viewable online [here](https://drive.google.com/file/d/14MtOL7b3iHPpHp_Xpvq9fhfwX_jckTjj/view?usp=sharing).

## Other Resources
### Dataset
The dataset used in the conducted research was the Br35H dataset. The dataset can be found and downloaded [here](https://www.kaggle.com/datasets/ahmedhamada0/brain-tumor-detection). The data was restructured into tumorous and non-tumorous images for the purpose of simplification. The images were used for both the generation of artificial images and then divided up for use in the evaluation of the atificial images via the convolutional neural network.

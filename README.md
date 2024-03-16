# UWEC - GAN Generated MRI Research
Contributors: [Tanner Hall](https://github.com/Tanner-2020), [Elena Bourget](https://github.com/elenabourget), [Kayla Behnke]()

## Overview
This research is designed to implement and evaluate several different strategies of image generation for the creation of MRI brain scans and their use in training the accuracy of a convolutional neural networks that is used to detect if an image contains a tumor in it in order to assist medical professionals.

## Projects
The code developed for this research can be broken into several parts. Firstly, each of the GAN techniques are independant programs designed to be run independantly. Each of these contains slight variation but start and end with the same input parameters and returned results. The other code consists of convolutional neural networks. The first implementation is a visualization of accuracy and visualizes the results, while the second is the an ehhnaced implementation that measures more metrics and untilized k-fold cross validation. Each major component is listed below.

### GAN Models
Generative Adversarial Networks (GANs) are used to create new, unqiue outputs from a set of input data. In this research, the GAN models are used to generate MRI images to add to a dataset for training data.

#### DC GAN
**Developed by: Tanner Hall**  
A Deep Convolutional GAN (DC GAN) is a model that utilizes a standard generator and discriminator dynamic as well as general loss. DC GAN does suffer from some issues, such as mode collapse. This can be caused by several factors, like catastrophic forgetting in the discriminator, allowing for the generator to produce images that are too similar to result in substantial additional data. The DC GAN used in this research was adapted from the implementation on TensorFlow's website

#### Unrolled GAN
**Developed by: Kayla Behnke**  
Unrolled GAN is a model that seeks to combat some of the shortcomings of DC GAN. This is done through the process of unrolling the discriminator, which allows it to anticipate the generator, resulting in a theoretical increase in the diversity of results from the GAN. This model can be implemented by modifying a standard DC GAN, such as that mentioned in the previous sub-section.

#### W GAN
**Developed by: Elena Bourget**  
A Wasserstein GAN (W GAN) is another way to get around the shortcomings of other GANs. This is done by the use of the Wasserstein distance metric. This metric allows for more stability in the training of the generative model. Like with Unrolled GAN, the purpose of these generative differences is to increase the variety of images.

### Convolutional Neural Network
The convolutional neural network used in this research is used to evaluate the improvements of metrics with the addition of various artifical images created by the GAN models.

#### Initial Implemention
**Developed by: Tanner Hall, Kayla Behnke, and Elena Bourget**  
The convolutional neural network, based on the example provided by TensorFlow (see resources), was used for inital assessment of the addition of artifiial data into the dataset. This project displays the accuracy visually and only runs a single trial. Because of the limitations in both speed and detail, this inital implementation was abandoned, but served as the basis for the modified implementation.

#### Modified Implementation
**Developed by: Tanner Hall and Kayla Behnke**  
The modified convolutional neural network features various improvements over the inital implementation. Firsty, the program features k-fold cross validation in an 8 traning and 2 testing division on the original, real images. This results in a large increase in the number of trials runs conducted on the artifical images and allows for more reliable metrics to be achieved. This implementation also includes the addition of various metrics, like accuracy, precision, recall, and f-score. This enables a larger numerical analysis of the results collected by the model.

## Reports
An inital report presentation was created in spring 2023 for use at the National Conference on Undergraduate Research (NCUR) held at the University of Wisconsin - Eau Claire. A poster was showcased to outline the results of the research. The poster is viewable online [here](https://drive.google.com/file/d/14MtOL7b3iHPpHp_Xpvq9fhfwX_jckTjj/view?usp=sharing).

## Other Resources
### Dataset
The dataset used in the conducted research was the Br35H dataset. The dataset can be found and downloaded [here](https://www.kaggle.com/datasets/ahmedhamada0/brain-tumor-detection). The data was restructured into tumorous and non-tumorous images for the purpose of simplification. The images were used for both the generation of artificial images and then divided up for use in the evaluation of the atificial images via the convolutional neural network.

### Code
The DC GAN model, as well as the basis of the Unrolled GAN, is based off of the tutorial by TensorFlow that can be found [here](https://www.tensorflow.org/tutorials/generative/dcgan).
The convolutional neural network is based off of the tutorial by TensorFlow and can be accessed [here](https://www.tensorflow.org/tutorials/images/cnn).

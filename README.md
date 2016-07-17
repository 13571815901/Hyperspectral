Deep Learning for Land-cover Classification in Hyperspectral Images
===================================================================

Hyperspectral images are images captured in multiple bands of the electromagnetic spectrum. This project is focussed at the development of Deep Learned Artificial Neural Networks for robust landcover classification in hyperspectral images. Land-cover classification is the task of assigning to every pixel, a class label that represents the type of land-cover present in the location of the pixel. It is an image segmentation/scenelabeling task. The following diagram describes the task.

<hr>

<img src="https://github.com/KGPML/Hyperspectral/blob/master/images/landcover-classification.png?raw=True" width="800"> 

Convolutional Neural Network
----------------------------

(CNN or ConvNet) are a special category of artificial neural networks designed for processing data with a gridlike structure. The ConvNet architecture is based on sparse interactions and parameter sharing and is highly effective for efficient learning of spatial invariances in images. There are four kinds of layers in a typical ConvNet architecture: convolutional (conv), pooling (pool), fullyconnected (affine) and rectifying linear unit (ReLU). Each convolutional layer transforms one set of feature maps into another set of feature maps by convolution with a set of filters.

Architecture of Convolutional Neural Network used
-------------------------------------------------

**input- [conv - relu - maxpool] x 2 - [affine - relu] x 2 - affine - softmax**
(Schematic representation below)

<img src="https://github.com/KGPML/Hyperspectral/blob/master/images/architecture.png?raw=True" width="800">

The system was trained on a machine with dual Intel Xeon E5-2630 v2 CPUs, 32 GB RAM and NVIDIA Tesla K-20C GPU. 

Dataset
-------

We have performed our experiments on the [Indian Pines Dataset](https://engineering.purdue.edu/~biehl/MultiSpec/hyperspectral.html). The following are the particulars of the dataset: 

* Source: AVIRIS sensor
* Region: Indian Pines test site over north-western Indiana
* Time of the year: June
* Wavelength range: 0.4 – 2.5 micron
* Number of spectral bands: 220
* Size of image: 145x145 pixel
* Number of land-cover classes: 16

Specifics of the learning algorithm
-----------------------------------

The following are the details of the learning algorithm used:

* Parameter update algorithm used: Mini-batch gradient descent
	* Batch size: 100
	* Learning rate: 0.01

* Number of steps: until best validation performance

<hr>

Performance
-----------

<img src="https://github.com/KGPML/Hyperspectral/blob/master/images/accuracy-bar.png?raw=True" width="800"> 

<img src="https://github.com/KGPML/Hyperspectral/blob/master/images/decoding.png?raw=True" width="800"> 

<hr>

<hr>

Description of the toolbox
--------------------------

- ``
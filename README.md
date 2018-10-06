# Pytorch-VGG-19

Using Pytorch to implement VGG-19

## Instruction

Implementation and notes can be found [here](https://github.com/Aleadinglight/Pytorch-VGG-19/blob/master/VGG_19.ipynb).

This is an implementation of this [paper](https://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Gatys_Image_Style_Transfer_CVPR_2016_paper.pdf) in Pytorch.

This one was wrote using important ideas from Pytorch tutorial. I did my best to explain in detail the ideas in each section of the Python notebook. The maths and visual illustation can be found below.

## Maths

We will feed two pictures X and Y into the VGG-19 neural network. We will adjust the feature maps of these pictures to look closely to each other. Because the feature maps contain the style and content of the particular picture (Convolutional layer helps us to create more aspects of a picture). I explain it with more detail [here](https://github.com/Aleadinglight/Pytorch-VGG-19/blob/master/VGG_19.ipynb).

We have to minimize the style loss the make the picture X adopt the style of picture Y, also we need to minimize the content loss between the picture X itself so that the content stays and the style changes.

The features maps from X that we will use:

<img src="../master/picture/feature_layers_size.jpg" width="300">

Using the Gram matrix as feature correlation between _one pixel to all others_ in one picture, we can calculate the style loss.

<img src="../master/picture/Gram_matrix.jpg" width="300">

## Gallery

From

<img src="../master/picture/ava.png" width="300"> <img src="../master/picture/style.png" width="300">

To

<img src="../master/picture/ava_after.png" width="300">

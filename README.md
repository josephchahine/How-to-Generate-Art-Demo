# How-to-Generate-Art-Demo
## Setup for GPU

If you do not know how to configure TensorFlow to run on GPU, take a look a this [post](https://medium.com/@viveksingh.heritage/how-to-install-tensorflow-gpu-version-with-jupyter-windows-10-in-8-easy-steps-8797547028a4).
The current version (1.4) of TensorFlow doesn't work with CUDA 9.0, so make sure to download CUDA 8.0 (I installed cuda_8.0.61_win10.exe and its patch cuda_8.0.61.2_windows.exe). For cuDNN, I used the file cudnn-8.0-windows10-x64-v6.0.zip.
The training took less than 5 minutes on my laptop. My graphics card is a NVIDIA Quadro M1000M.

## Overview

This is the code for [this](https://youtu.be/Oex0eWoU7AQ) video on Youtube by Siraj Raval as part of the Intro to Deep Learning Nanodegree with Udacity. We're going to re-purpose the pre-trained VGG16 convolutional network that won the ImageNet competition in 2014 for image classification to transfer the style of a given image to another. [This](https://arxiv.org/abs/1508.06576) is the original paper on the topic.


## Dependencies

run `pip install -r requirements.txt` to install the necessary dependencies


## Usage

If it doesn't exist, create a file called ~/.keras/keras.json and make sure it looks like the following:

   ````
   {
       "image_dim_ordering": "tf",
       "epsilon": 1e-07,
       "floatx": "float32",
       "backend": "tensorflow"
   }
   ````

Then you can run the code via typing `jupyter notebook` into terminal


## Credits


The credits for this code go to [hnarayanan](https://github.com/hnarayanan/artistic-style-transfer) and to [Siraj Raval](https://github.com/llSourcell) who created a wrapper to get people started.





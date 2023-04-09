<!-- This is the markdown template for the final project of the Building AI course, 
created by Reaktor Innovations and University of Helsinki. 
Copy the template, paste it to your GitHub README and edit! -->

# My Project to Find flower as per my required size

Final project for the Building AI course

## Summary

My Project is about to find image from data set 
it will tell all the heads of data sets.
Also detail the total number of images in data set and in following picuter, if you want to see rose flower no 2 it will show you 



![image](https://user-images.githubusercontent.com/122665993/230756152-03fa8d50-5ccd-4e9c-8607-048fb50c8e41.png)


## Background

it Sort out your dificulty ? How common or frequent is this problem? What is your personal motivation? Why is this topic important or interesting?

This is how you make a list, if you need one:
I need a rose flowr from thousands 
i need only tupil
any one wants to pic a rose


## How is it used?

Simple process to use it copy the code and run 

Images will make your README look nice!
Once you upload an image to your repository, you can link link to it like this (replace the URL with file path, if you've uploaded an image to Github.)
![image](https://user-images.githubusercontent.com/122665993/230756267-73a9c01d-3c5e-46e7-b0f4-441377b4ffd8.png)

If you need to resize images, you have to use an HTML tag, like this:
![image](https://user-images.githubusercontent.com/122665993/230756275-54a5ddf7-4f60-428e-862f-91d94e54400f.png widt="300")

This is  code examples:
```
# these files are necessary to import as it is
import numpy as np
import os
import PIL
import PIL.Image
import tensorflow as tf
import tensorflow_datasets as tfds
import pathlib

# here you can load dataset what you want i have loaded a data set of flowers 
# do not do any thing more these are builtin you have to change only paths
dataset_url = "https://storage.googleapis.com/download.tensorflow.org/example_images/flower_photos.tgz"
archive = tf.keras.utils.get_file(origin=dataset_url, extract=True)
data_dir = pathlib.Path(archive).with_suffix('')

#this line will tell you how many roses are in the data set
image_count = len(list(data_dir.glob('*/*.jpg')))
print("there are total images",image_count);

# now set the size of image what you like
batch_size = 32
img_height = 180
img_width = 180



# now the result will be as follow
 #                                        there are total images 3670
  #                                        ['daisy', 'dandelion', 'roses', 'sunflowers', 'tulips']
# at this stage i know there are six classes in this data set namely above now i want to see the image of sunflowers at 2 number
flower = list(data_dir.glob('daisy/*'))
PIL.Image.open(str(flower[2]))

```


## Data sources and AI methods
if you want to see more please visit the following link
https://www.tensorflow.org/tutorials/load_data/images

you can use ['daisy', 'dandelion', 'roses', 'sunflowers', 'tulips']
where in code daisy written and also can change the number as you desire

## Challenges

What does your project _not_ solve? Which limitations and ethical considerations should be taken into account when deploying a solution like this?

## What next?

How could your project grow and become something even more? What kind of skills, what kind of assistance would you  need to move on? 


## Acknowledgments

* list here the sources of inspiration 
* do not use code, images, data etc. from others without permission
* when you have permission to use other people's materials, always mention the original creator and the open source / Creative Commons licence they've used
 
from PIL import Image, ImageFilter

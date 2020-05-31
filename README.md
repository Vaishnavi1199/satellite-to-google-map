# Satellite-to-google-map
This is a pix2pix (cGAN) model for translating satellite image to google map image.I tried to implement the original model from scratch.
The dataset consist of a folder"maps" which contains "train" and "val" as subfolders.Train containing 1096 and val 1099 images.
images were train and val were of size 600*1200 , where 1st half is satellite image and 2nd half is google map image.

# About pix2pix
Pix2Pix is a  **condtional Generative Adversarial Network (cGAN)** model designed for general purpose image-to-image translation.
Dataset link [link to downlod dataset!](http://efrosgans.eecs.berkeley.edu/pix2pix/datasets/maps.tar.gz)

The approach was presented by Phillip Isola, et al. in their 2016 paper titled “Image-to-Image Translation with Conditional Adversarial Networks”. Here is the link to original paper.
[link to original paper!](https://arxiv.org/abs/1611.07004)
The GAN architecture is comprised of a **generator model** for generating new plausible synthetic images, and a **discriminator model** that classifies images as real (from the dataset) or fake (generated). The discriminator model is updated directly, whereas the generator model is updated via the discriminator model. The two models are trained in an **adversarial manner** where the generator seeks to better fool the discriminator and the discriminator seeks to better identify the counterfeit images.



# Approach
**"image_to_numpy_array"**- loads train images, separates satellite and google map image, resize,normalize and put in separate lists and return the lists in form of array.
**"model_and_training"**- contains model architecture and training part.model architecture comprise of discriminator,generator, gan model.
training was done for 200 epochs .Subplots (of source,generated and expexted image) and generator model are saved after every 10 epochs in folders "subplot" and "g_model" respectively.
**"image_translation_of_some_examples"**-manually chose combination of few val examples and g_model and predicted generated google map image. subplot was saved in "val_subplots".

# My experience.
I have been working on a different pix2pix model during my internship since last month, and decided to try and implement it on this general dataset from scratch.It took me days to understand and implement, and after numerous failed attempts and long and frustrating training hours,this model gave fairly decent results.Although a little more access to computing power could have got it spot on.
Suggestions & feedbacks are welcomed!
Cheers to new learning!

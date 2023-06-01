## Overview
Using super-resolution techniques, such as U-Net and SRGAN, to build a video super-resolution model.
This Project is part of the course project for MIT 6.8300 Advances in Computer Vision.
All development and data originally stored on Google Drive and Google Colab.

## Intro and Structure
1. Train U-Net model using pairs of LR and HR image dataset.
2. Process video into the same dimension (256 * 256).
3. Complie the model with chosen metrics and loss function, either from pre-defined library function or user-defined fuction. Train with image dataset.
4. Read the HR resized video, blur with user-defined kernel size, and predict super-resolution image.
5. Generate SR video using predicted frames. That's the 1st version of SR video.
6. Compute optical flow using LR video. Generate interpolated frames.
7. Use frame_upscale to generate high resolution.
8. Use blend_interpolation_with_HR to blend upscaled interpolated frames with SR frames.
9. Combine the frames using either blending or stacking function.
10. Generate the final SR video. That's the 2nd version of SR video with temporal filtering technique.

##  Data
Kaggle pulic HR and LR image dataset is used to train both the U-net and SRGAN model. 

Source: Aditya Chandrasekhar, “Image super resolution,” Kaggle. Available: https://www.kaggle.com/datasets/adityachandrasekhar/image-super-resolution. Aug. 2020.

## SRGAN model 
Source: Ledig, Christian, et al. "Photo-realistic single image super-resolution using a generative adversarial network." Proceedings of the IEEE conference on computer vision and pattern recognition. 2017.

A SRGAN model that's almost identical to the paper above was trained with the same training image dataset that's used for U-net. 

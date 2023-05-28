# CV_Video_Super-resolution
Computer Vision project building a video super-resolution model from U-Net and SRGAN
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
HR and LR Image Dataset used to train the U-Net model. All images have size 256 * 256.
https://drive.google.com/drive/folders/1P9uBlGoEbSs7Y4U5DTxlg6TPNG02sBEg?usp=share_link

## To be completed
SRGAN model update

# Deepfake Detection

## About

This project was created in 2021 fall semester for AIT Deep Learning course at AIT. The authors are Christina Wang and Isabel Grondin. 

## Description

The goal of our project is to detect videos that are deepfakes.  For the first stage of our project, we are using the first jpg frame of these videos to train our model and determine if the video is a deep fake or not. In the second stage, we plan on extracting multiple frames from the video and using the average prediction value to determine if the video is real or fake. 


## The Data

Our project utilizes the following data set:
[Celeb Deepfake Dataset](https://github.com/yuezunli/celeb-deepfakeforensics)

We are only utlizing the Celeb Deepfake 1 dataset, which includes a combination of 1203 real and fake/synthesized videos of celebrities from Youtube. We broke down all the videos into jpg images and standardized their sizes and modes.


## Milestone 1

**Finding and Processing the Data**

At the outset, we knew that we wanted to pursue a project in deepfake detection. As celebrty deep fakes are becomming increaly common, we decided to choose a dataset that was geared towards detecting celebrity deepfakes. We initally found our dataset through paper with code and have linked the github page for the data above. 

Our dataset came in the form of videos, so our first step was extracting the videos into sets of indivudual frames. Then for the purpose of consistency, we standardized the size and mode of all the images, taking into to consideration that the photos retained the same proportions. Here is a sample of a photo before and after our preprocessing procedure:
![Screen Shot 2021-10-07 at 11 11 24 PM](https://user-images.githubusercontent.com/60895491/136463965-cd2c135c-5dc4-4346-bb26-8876508b32c1.jpeg)

Finally, we split the data into train and test sets.

## References


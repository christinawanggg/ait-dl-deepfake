# Deepfake Detection

## About

This project was created in 2021 fall semester for AIT Deep Learning course at AIT. The authors are Christina Wang and Isabel Grondin. 

## Description

The goal of our project is to detect videos that are deepfakes.  For the first stage of our project, we are using the first jpg frame of the videos contained in the Celeb Deepfake Dataset to train our model to determine if the video is a deep fake or not. In the second stage, we plan on extracting multiple frames from the video and using the average prediction value to determine if the video is real or fake. 


## The Data

Our project utilizes the following data set:
[Celeb Deepfake Dataset](https://github.com/yuezunli/celeb-deepfakeforensics)

We are only utlizing the Celeb Deepfake 1 dataset, which includes a combination of 1203 real and fake/synthesized videos of celebrities from Youtube. We broke down all the videos into jpg images and standardized their sizes and modes.


## Milestone 1

**Finding and Processing the Data**

At the outset, we knew that we wanted to pursue a project in deepfake detection. As celebrty deep fakes are becomming increasingly common, we decided to choose a dataset that was geared towards detecting celebrity deepfakes. We initally found our dataset through papers with code and have linked the github page for the data above. 

Our dataset came in the form of videos, so our first step was extracting the videos into sets of indivudual frames. Then for the purpose of consistency, we standardized the size and mode of all the images, taking into to consideration that the photos retained the same proportions. Here is a sample of a photo before and after our preprocessing procedure:
![Screen Shot 2021-10-07 at 11 11 24 PM](https://user-images.githubusercontent.com/60895491/136463965-cd2c135c-5dc4-4346-bb26-8876508b32c1.jpeg)

Finally, we split the data into train and test sets.

## Milestone 2

**Training data and evaluating results**

During this milestone, we created and initial model. We originally used a CNN model, but our accuracy only ended up being .67 at the highest, which is equivalent to our model just learning to guess an image is fake for all the images. The split between our real and fake data is apprx. 33% to 67%. We adjusted our model to use InvceptionV3 as a base and then added and additional dense layer and dropout layer. We also added augmented data to our training set. With this updated model we were able to achieve .88 accuracy on our test set. Also, our loss was quite small meaning that our predictions wer strong overall. Here is a confusion matric of our predicitons: 

<img width="361" alt="Screen Shot 2021-11-18 at 1 45 49 PM" src="https://user-images.githubusercontent.com/60895491/142417858-5ff442cf-78cd-4307-aa2b-45e0cb4d5ab7.png">

<img width="167" alt="Screen Shot 2021-11-18 at 1 46 28 PM" src="https://user-images.githubusercontent.com/60895491/142417952-73570e0c-0bcf-4419-a494-7a8805815ec4.png">

We definitely experienced more false negatives than false positives. While it is not ideal the have any false negatives and false positives, it is better to have more false negatives because that means we are guessing it is fake when it is actually real. As far as we are concerned, this is less damaging than the opposite case. 


## References


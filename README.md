# Image_Segmentation_FCN8_VGG16_CamVid
This repository illustrates how to build a Fully Convolutional Neural Network for semantic image segmentation.  We will train the model on a custom dataset prepared by divamgupta. This contains video frames from a moving vehicle and is a subsample of the CamVid dataset.  We will be using a pretrained VGG-16 network for the feature extraction path, then followed by an FCN-8 network for upsampling and generating the predictions. The output will be a label map (i.e. segmentation mask) with predictions for 12 classes. 

The FCN8 model looks like this:

![image](https://user-images.githubusercontent.com/64538407/112112404-270ad300-8bbe-11eb-8b3a-3212bb66ae35.png)


The annotated input data:

![image](https://user-images.githubusercontent.com/64538407/112112290-017dc980-8bbe-11eb-940c-90913d5d000c.png)


After 30 epochs the results are as the following:

![image](https://user-images.githubusercontent.com/64538407/112112515-4ace1900-8bbe-11eb-9000-d7d8d83ad986.png)

The IoU for each class:

sky            0.8523710373675862 
building       0.4478193732096381 
column/pole    9.144156908767303e-05 
road           0.7111443882761425 
side walk      0.0015516153206296484 
vegetation     0.009442092266299934 
traffic light  2.990072956886116e-10 
fence          1.0303223877690097e-10 
vehicle        0.005194000655137685 
pedestrian     3.950890915431674e-05 
byciclist      1.4382074180670196e-10 
void           0.0006814312320996181 



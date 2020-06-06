## Machine Learning Engineer Nano degree Capstone Project
## Dog breed classifier with RESNET50 
#### by Zhenyue Zhu
#### 06/05/2020

### Objective
When a user uploads an image to the web server. The machine learning model will act on the backend. 
The task includes following stages:
* Detect if the image has dog faces, if so, determine what breed the 
dog is.
* If it detects a human face, the algorithm will determine the most 
resembling dog breeds for the human’s face.   
* If neither human nor dog face is detected from the image, it will show 
a error mesage.

### Method
* To detect a human face, I directly used openCVs haar feature based cascade classifier.
* To detect a dog face, I use pretrained VGG16 model which is used to identify 1000 different types of objects. Index from 151 and 268 are different dog breed index. 
* To classifier dog faces. I create a transfer learning model  
RESNET50 to only train the last fully connected layer for dog breeds 
classifier. 
* Finally combine all above methods to achieve the goal of this project. 

### Dataset
Since I only use to train my own dog classifier model, I only need the 
datasets with all dog images. So I am using the data provided by 
Udacity, where there are 133 dog breeds with a total of 8351 dog images. 
Training: 6680 images. 
Validation: 835 images.
Test: 836 images.
Each dog breed for the training/validation/test datasets are in a 
separate folder. The dataset is kind of unbalanced, some breeds have 
more images than others. Also, these images have different sizes. 
 

## Results of the model

For this project, I finally decided to use restnet50 model for transfering learning purpose. 
Where I set the calculation to train the model only on the last layer, after 10 epochs, 
the accuracy of the model is already more than 80%, which is much, much better than the CNN model that I 
built from scratch (accuracy = 12%). 



# Reconstructing-Training-Data-From-Trained-Neural-Network

This repository contains implementation of a research paper - Reconstruction Training Data from Trained Neural Network.
To understand it more deeply you can check the original paper which is present in this repository named Research-Paper.pdf.

Lets firstly understand the basic idea of this paper

### Overview of the paper
Usually, what we do is train a Neural Network using some training data and then leverage it to predict the output for some unknown data.
But, this paper has done some great work to extract the training data back from the trained model.

Lets understand this more concisely,

Input to us is a Trained MLP model. By trained MLP model we actually mean that we have the weights/parameters saved with us. 
Now ,just by using this we have to generate the training data used while training our model.

<img width="1134" alt="image" src="https://github.com/hsahuja111/Reconstructing-Training-Data-From-Trained-Neural-Network/assets/43888676/c3f720e9-6eb6-442d-8082-fb4de385eb8a">


### Maths Behind
In the actual training process of a Neural Network we apply gradient descent on the Loss function we got. 
This loss function is actually the difference between the predicted and original.
We keep on iterating till the time we got minimum error.

But here, What will be our Loss functions??

The intuition of it lies in the fact that every MLP model although seems to be generic but often has some bias.
In case of Binary MLP model trained with Gradient descent, it converges to the same solution as given by SVM margin maximising.
Hence from the equation given by SVM Margin Maximing problem we have derived 2 loss functions for our problem. The 3rd Loss function is based upon generic thinking.

So this is the SVM equation:

<img width="568" alt="image" src="https://github.com/hsahuja111/Reconstructing-Training-Data-From-Trained-Neural-Network/assets/43888676/3269e53e-2dfb-4e57-9fc6-c64c383231bc">


<img width="350" alt="image" src="https://github.com/hsahuja111/Reconstructing-Training-Data-From-Trained-Neural-Network/assets/43888676/33d1d9b6-ae21-4606-9092-8753c5ce1fee">


![image](https://github.com/hsahuja111/Reconstructing-Training-Data-From-Trained-Neural-Network/assets/43888676/454b7b28-fded-47a9-9b6e-780dab1c4436)

So here there are two 

### 3 Loss functions used
#### 1.Parameter Loss
<img width="369" alt="image" src="https://github.com/hsahuja111/Reconstructing-Training-Data-From-Trained-Neural-Network/assets/43888676/6b1f1b08-f128-411f-b40a-6a9e88f25c2d">


#### 2.Lambda Loss
<img width="265" alt="image" src="https://github.com/hsahuja111/Reconstructing-Training-Data-From-Trained-Neural-Network/assets/43888676/5a490fa2-bf62-4a3c-9621-ddbeabf9ce39">

#### 3.Range Loss
Say, our training data were gray scale image so the pixel range will lies from -1 to 1. So we are penalising if we our resultant images goes outside of this range.









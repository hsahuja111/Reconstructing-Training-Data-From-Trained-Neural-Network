# Reconstructing-Training-Data-From-Trained-Neural-Network

This repository contains implementation of a research paper - Reconstruction Training Data from Trained Neural Network.
To understand it more deeply you can check the original paper which is present in this repository named Research-Paper.pdf.

* Lets firstly understand the basic idea of this paper

### Overview
Usually, what we do is to train a Neural Network using some training data and then leverage it to predict the output for some unknown data.
But, this paper has done some great work to extract the training data which we have used to train.

Lets understand this

Input to us is a Trained MLP model. By trained MLP model we actually mean that we have the weights/parameters saved with us. 
Now , just by using this we have to generate the data which was used in the training time to train it.

### Maths Behind
In the actual training process of a Neural Network we apply gradient descent on the Loss function we got. 
This loss function is actually the difference between the predicted and original.
We keep on iterating till the time we got minimum error.

But here, What will be our Loss functions??

#### 3 Loss functions used





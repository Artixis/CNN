# Stucture of CNN

[Main](https://github.com/Artixis/CNN/blob/main/README.md)


A typical CNN py. file with have the following structure:

- Imports 
These include the usual imports along with various torch libraries. 

- CNN Definition

This is essentially a class definition in which we decide how the CNN will work. More specifically we define the layers and what to do within those layers. 

- Convolutional Layer (Within the CNN definition)

Start with the convolutional layers. For the CIFAR10 data set out for convolutional layer has in_channels=3, because of the RBG colouring of the images, out_channels=32, since each image in 32 by 32 pixels. The kernel_size is subject to change but have seen quite a few implementations with the kernal equal to 3 or 5.
<br> 
Then run the function BatchNorm2d(32) - for the 32 out_channels. I'm not exactly sure if this is necessary for a CNN over CIFAR10 but eh. 
<br>
"*BatchNorm2d computes the mean and standard deviation per channel*" 

We then apply our first activiation function on the neurons. This could be ReLU, Sigmoid, tanh etc. 
<br> 
The smallCNN code defines these as *nn.ReLU(inplace=True)* where inplace saves computational time(potentially). 
<br> 
The third type of function we see in the convolutional layer is MaxPool2d, this determines how the model slides over the pixels. For instance, say with have an image we're scanning over, is we set max pooling to 2 by 2, we will slide or convolute over 4 cells at a time. 

> Might be useful to include an image here 

- fc_layer (Also in CNN definition) 

Note quite sure what fc is meant to mean, ask Yi. This layer seems similar to the MLP model. In that, we have different layers and activation functions, one after the other, ending with a solver(like softmax).











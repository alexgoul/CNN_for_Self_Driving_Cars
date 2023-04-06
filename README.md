# CNN_for_Self_Driving_Cars

The objective of this project is to recognize the traffic signs from the images. These traffic signs can be a stop or a danger sign or a sign that denotes the speed limit. The traffic sign recognition is very important for self-driving cars and autonomous vehicles to operate on roads.
With these in our mind, it is necessary to make sure it identifies the images with a high degree of accuracy. If it fails to do so, then the results it will be very dangerous for our safety.
Therefore, we build a convolutional neural network that classify traffic, sign images into their respective categories. We will use the google colab to built our traffic sign classification project.

**Import Libraries**

First, we import some important libraries for our project. We will use keras to import the necessary layers and optimizer for our convolutional neural network.
The matplolib.pyplot, seaborn and cv2 will be used to visualize our data and results. We will load our data set with pickle library and pandas to read our csv file.
Lastly, we import random to generate random numbers and of course numpy. 

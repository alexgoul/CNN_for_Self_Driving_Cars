# CNN_for_Self_Driving_Cars

The objective of this project is to recognize the traffic signs from the images. These traffic signs can be a stop or a danger sign or a sign that denotes the speed limit. The traffic sign recognition is very important for self-driving cars and autonomous vehicles to operate on roads.
With these in our mind, it is necessary to make sure it identifies the images with a high degree of accuracy. If it fails to do so, then the results it will be very dangerous for our safety.
Therefore, we build a convolutional neural network that classify traffic, sign images into their respective categories. We will use the google colab to built our traffic sign classification project.

**Import Libraries**

First, we import some important libraries for our project. We will use keras to import the necessary layers and optimizer for our convolutional neural network.
The matplolib.pyplot, seaborn and cv2 will be used to visualize our data and results. We will load our data set with pickle library and pandas to read our csv file.
Lastly, we import random to generate random numbers and of course numpy.

**Image Pre-processing**

We convert the images in to grayscale for reducing the computation, since the colors are not realy important for trafic signs. The important details are the age and shift of the images. Next we apply the histogram equalization technique to standarize the lighting and last we normalize the pixel between zero and one by dividing them by 255. The image on the left is after pre-processing and on the right before:
![download (1)](https://user-images.githubusercontent.com/128620549/236262819-4c87beaa-f2ed-4345-87bb-b128d9f470ba.png)
![download (2)](https://user-images.githubusercontent.com/128620549/236262791-4a469a2f-32dd-445b-9602-3908b8007674.png)

**convolutional Neural Network

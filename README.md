# CNN_for_Self_Driving_Cars

The objective of this project is to recognize the traffic signs from the images. These traffic signs can be a stop or a danger sign or a sign that denotes the speed limit. The traffic sign recognition is very important for self-driving cars and autonomous vehicles to operate on roads.
With these in our mind, it is necessary to make sure it identifies the images with a high degree of accuracy. If it fails to do so, then the results it will be very dangerous for our safety.
Therefore, we build a convolutional neural network that classify traffic, sign images into their respective categories. We will use the google colab to built our traffic sign classification project.

**Import Libraries**

First, we import some important libraries for our project. We will use keras to import the necessary layers and optimizer for our convolutional neural network.
The matplolib.pyplot, seaborn and cv2 will be used to visualize our data and results. We will load our data set with pickle library and pandas to read our csv file.
Lastly, we import random to generate random numbers and of course numpy.

**Image Pre-processing**

We convert the images in to grayscale for reducing the computation, since the colors are not realy important for trafic signs. The important details are the age and the shift of the images. Next we apply the histogram equalization technique to standarize the lighting and we normalize the pixel between zero and one by dividing them by 255. The image on the left is after pre-processing and on the right before:
![download (1)](https://user-images.githubusercontent.com/128620549/236262819-4c87beaa-f2ed-4345-87bb-b128d9f470ba.png)
![download (2)](https://user-images.githubusercontent.com/128620549/236262791-4a469a2f-32dd-445b-9602-3908b8007674.png)

**Convolutional Neural Network**

We construck our Convolutional Neural Network with keras and it will have the following architecture:
![CNN_structure](https://user-images.githubusercontent.com/128620549/236953596-1af9a80b-befc-4441-9e1d-d43c53b01055.png)

Before we feed our input data to the densely fully connected artificial neural network, we perform some procces to our data from the two convolutional blocks. In the two blocks, first we appply the convolution which extracts the  features out if the input image. The ReLU activation function will rectified our layer unit. Any value less than zero will be set to zero and any which is positive will be passed along. We apply the activation function to improve sparcity of the feature mass, which improves the performance of the network. Next, we down sampling the dimension of the image with the max pooling layer, which picks the max number of each pixel. The Droppout layer reduce the validation loss and the flatten layer in the last block reshape the data from two dimensions to one.\
In the first conv block: the number of filters= 32, size of filter= (5,5), input shape= (32,32,1)\
In the second conv block we double the filter size to 64. After we flatten the output and pass it to the fully connected layer, we dense the output with a softmax activation function.
\
Then we complie our model with adam optimizer and we select 'sparse_categorical_crossentropy' loss, because with have more then 42 classes in our model. After we train our model in 50 epochs we can see that our accuracy=92% and validation accuracy=94% which is very high. In the evaluation of the model the test accuracy are 93% which is very high number. Lastly we visualize our model loss and accuracy results in the following diagrams:

![Model_accuracy](https://user-images.githubusercontent.com/128620549/236963619-7a1b4128-6cdd-40af-a0cb-4bc79ba6e45d.png)
![Model_loss](https://user-images.githubusercontent.com/128620549/236963622-ff3c29f6-6887-4874-99a0-5e54acf7601d.png)

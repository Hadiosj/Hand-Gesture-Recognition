### Training a Neural Network to Detect Gestures with OpenCV in Python

In this project, we discuss efforts that resulted in a system that takes advantage of Convolutional Neural Networks to recognize hand gestures based on depth images captured by the camera. It is intended to support and use technologies especially in the field of education and translation for helping deaf and mute people to communicate with ease. The program is developed using a science field of computer vision, as well as additional libraries which are: Tensorflow, Numpy, keras and OpenCV.

![alt text](link here)

#### Training the model

VGG16 has a very good architecture for benchmarking on a particular task, while also being available freely on the internet, which makes it a convenable choice for various applications, thus we end up using it in this project.

![alt text](link here)

A convolutional neural network is built using Keras & TensorFlow. Starting with the VGG-16 pre-trained model, and adding 4 dense layers along with a dropout layer on top.
The model is then saved and loaded into a hdf5 file.

#### Executing the model on live hand gestures

The technique used to extract gestures from real time images is ‘background subtraction’, a common and widely used technique for generating a foreground mask (namely, a binary image containing the pixels belonging to moving objects in the scene) by using static cameras. As the name suggests, BS calculates the foreground mask performing a subtraction between the current frame and a background model, containing the static part of the scene or, more in general, everything that can be considered as background given the characteristics of the observed scene.
Background subtraction is implemented using the libraries OpenCV to use the feed from a camera connected to the computer, and the copy library to detect and draw contours of the hand.

Background Initialization:
![alt text](link here)

Background Update:
![alt text](link here)

Finally, the prediction of the gesture detected is made and the result is translated to a text written in a separate .txt file which can be directly used for chat and communication, in addition to displaying the prediction and its level of confidence on the screen:

![alt text](link here)
![alt text](link here)
![alt text](link here)
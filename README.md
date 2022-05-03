
# Image Captioning Using LSTM

The goal of this project is to generate some information relevant to the image provided as input. With the help of deep learning combined with image processing, we thought of combining those two and generating some proper output related to that.
## Result
The model generates a suitable caption for the input image with an accuracy of 56.2%

![MOdel Output](https://github.com/yogesh-vishwakarma/Image-Captioning-using-LSTM/blob/master/Resources/3.JPG)

Here in above image, the input image is in the left with generated output on right.

## Architecture
Feature Extraction Model:

![MOdel Output](https://github.com/yogesh-vishwakarma/Image-Captioning-using-LSTM/blob/master/Resources/4.JPG)

### VGG-16 Architecture
The convolution layer consists of 3*3 filters and the stride length is fixed at 1. Max pooling is done using a 2*2-pixel window with a stride length of 2. All the images need to be converted into a 224*224-dimensional image.
![MOdel Output](https://github.com/yogesh-vishwakarma/Image-Captioning-using-LSTM/blob/master/Resources/6.JPG)

### training Model
Long Short Term Memory(LSTM) is a special type of RNN’s, capable of Learning long-term dependencies.LSTM has the nature of remembering information for long periods of time as their default behavior. 

![MOdel Output](https://github.com/yogesh-vishwakarma/Image-Captioning-using-LSTM/blob/master/Resources/rnn.jpeg)

### Work Flow:

1.  Image Preprocessing
2.  Creating Feature Extraction Model.
3.  Generate Feature Vector
4.  Train the model with LSTM 
5.  Test the model using BLUE score.

## Training Dataset
Used Flicker8k for training and testing. The dataset contains 6000 training images, 1000 development images, and 1000 test images. Other datasets like Flickr30k and MSCOCO for image captioning exist but both these datasets have more than 30000 images thus processing them becomes computationally very expensive and time consuming. 
Training Dataset Image and 5 suitable captions.
![MOdel Output](https://github.com/yogesh-vishwakarma/Image-Captioning-using-LSTM/blob/master/Resources/5.JPG)

## Tools Used:
The project was done in python3 using NumPy, phyttsx, Keras, etc.
Implementation is done using VGG-16 architecture in CNN and LSTM as  RNN.
We used the BLUE score for checking the accuracy of our model which used the Natural Language Toolkit (NLTK).


## Limitations

Due to our low computational power we used a relative feasable dataset for our training model which provided us some Limitations.
![image1](https://github.com/yogesh-vishwakarma/Image-Captioning-using-LSTM/blob/master/Resources/1.JPG)

the classifier was confused due to a similar color in the entire
image. In the figure below the model predicts water but also detects a dog in the image
however a dog is not present in the image

![image1](https://github.com/yogesh-vishwakarma/Image-Captioning-using-LSTM/blob/master/Resources/2.JPG)

In some other cases, it tried to confuse the classifier with an ambiguous image of a rabbits
face morphed on a lion and it detects a dog with a red ball (referring to the red nose of
the rabbit.

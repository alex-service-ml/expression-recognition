# Expression Recognition with TensorFlow  
## Introduction
The purpose of this repository is to become familiar with TensorFlow and explore using my own dataset, 
along with the issues of doing so. The dataset itself has not been uploaded for various reasons, but I do 
describe how the data was generated, which should be easy enough to recreate.  

## The Approach  
With TensorFlow, I built a simple Convolutional Neural Network consisting of two conv-layers followed by 2 
fully-connected layers. The convolutional layers use a significantly small number of features (8 and 16), 
whereas the fully-connected layers are exorbitantly large compared to current common networks, such as ResNet50. 
Otherwise, it is a fairly typical network, using:
-ReLU activations
-dropout
-softmax
-categorical cross-entropy  

## The Data
There are 10 total labels, including happy, angry, silly, etc. At the time of training, I used roughly 2000 images, 
but a large caveat is that they were all extracted from one video clip, which ultimately results in a failure to 
generalize (the network overfits on the training set). In short, the network is fantastic at recognizing facial 
expressions within the context of the video (even clips I haven't trained on), but outside of that, it will fail 
miserably. At some point, I would like to return and perform this experiment again, except with new data and a 
more modern deep learning architecture.

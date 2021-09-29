### Messy vs. Clean Room Detection Project with Convolutional Neural Network VGG19 
<a id="data-source"></a>
Judy Chen

Link to Code: <br>
https://github.com/jchen9619/Convolutional-Neural-Network-for-Messy-Clean-Room-Detection/blob/main/Messy%20vs%20Clean%20Room%20.ipynb

**Introduction** <br>
Using Tensorflow, this project examines the accuracy of the CNN module VGG19 on predicting the binary output of detecting if a room is messy or clean.

**Dataset** <br>
The training set comprises 212 images, half labeled "clean" and half labeled "messy", of which 20% was used as a validation dataset in the training process. The test set includes 10 images. 

**Modeling: Neural Network Layers** <br>
In addition to Keras preset model VGG19, the final two Dense layers use ReLu and Sigmoid activation functions after flattening the VGG19 output. Additionally, a callback parameter was included when fitting the model to stop the training process when training accuracy achieved 90%. 

The model summary is as follows: <br>

Layer (type)                 Output Shape              Param #   
=================================================================
input_1 (InputLayer)         [(None, 32, 32, 3)]       0         
_________________________________________________________________
block1_conv1 (Conv2D)        (None, 32, 32, 64)        1792      
_________________________________________________________________
block1_conv2 (Conv2D)        (None, 32, 32, 64)        36928     
_________________________________________________________________
block1_pool (MaxPooling2D)   (None, 16, 16, 64)        0         
_________________________________________________________________
block2_conv1 (Conv2D)        (None, 16, 16, 128)       73856     
_________________________________________________________________
block2_conv2 (Conv2D)        (None, 16, 16, 128)       147584    
_________________________________________________________________
block2_pool (MaxPooling2D)   (None, 8, 8, 128)         0         
_________________________________________________________________
block3_conv1 (Conv2D)        (None, 8, 8, 256)         295168    
_________________________________________________________________
block3_conv2 (Conv2D)        (None, 8, 8, 256)         590080    
_________________________________________________________________
block3_conv3 (Conv2D)        (None, 8, 8, 256)         590080    
_________________________________________________________________
block3_conv4 (Conv2D)        (None, 8, 8, 256)         590080    
_________________________________________________________________
block3_pool (MaxPooling2D)   (None, 4, 4, 256)         0         
_________________________________________________________________
block4_conv1 (Conv2D)        (None, 4, 4, 512)         1180160   
_________________________________________________________________
block4_conv2 (Conv2D)        (None, 4, 4, 512)         2359808   
_________________________________________________________________
block4_conv3 (Conv2D)        (None, 4, 4, 512)         2359808   
_________________________________________________________________
block4_conv4 (Conv2D)        (None, 4, 4, 512)         2359808   
_________________________________________________________________
block4_pool (MaxPooling2D)   (None, 2, 2, 512)         0         
_________________________________________________________________
block5_conv1 (Conv2D)        (None, 2, 2, 512)         2359808   
_________________________________________________________________
block5_conv2 (Conv2D)        (None, 2, 2, 512)         2359808   
_________________________________________________________________
block5_conv3 (Conv2D)        (None, 2, 2, 512)         2359808   
_________________________________________________________________
block5_conv4 (Conv2D)        (None, 2, 2, 512)         2359808   
_________________________________________________________________
block5_pool (MaxPooling2D)   (None, 1, 1, 512)         0         
_________________________________________________________________
flatten (Flatten)            (None, 512)               0         
_________________________________________________________________
dense (Dense)                (None, 224)               114912    
_________________________________________________________________
dense_1 (Dense)              (None, 1)                 225       
=================================================================
Total params: 20,139,521
Trainable params: 115,137
Non-trainable params: 20,024,384
_________________________________________________________________


**Conclusion** <br>
Of the 10 test set images, the CNN model successfully predicted the status of 6. Two of the wrong predictions are misleading pictures of messy rooms that can easily be mistaken as clean, as they both show objects with clealry defined edges. 

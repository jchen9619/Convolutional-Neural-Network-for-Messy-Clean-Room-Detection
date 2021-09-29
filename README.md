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
  <img src="https://github.com/jchen9619/Convolutional-Neural-Network-for-Messy-Clean-Room-Detection/blob/main/CNN%20VGG19%20Param.png" />
</p>

**Conclusion** <br>
Of the 10 test set images, the CNN model successfully predicted the status of 6. Two of the wrong predictions are misleading pictures of messy rooms that can easily be mistaken as clean, as they both show objects with clealry defined edges. 

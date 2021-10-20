### Messy vs. Clean Room Detection Project with Convolutional Neural Network VGG19 
---
<a id="data-source"></a>
Judy Chen

[Full Code](https://github.com/jchen9619/Convolutional-Neural-Network-for-Messy-Clean-Room-Detection/blob/main/Files/Messy%20vs%20Clean%20Room%20.ipynb)

**Introduction** <br>
Using Tensorflow, this project examines the accuracy of the CNN module VGG19 on predicting the binary output of detecting if a room is messy or clean.

**Dataset** <br>
The training set comprises 212 images, half labeled "clean" and half labeled "messy", of which 20% was used as a validation dataset in the training process. The test set includes 10 images. 

Below is a sample of 10 images in the training set: <br>
**Messy** <br>
![messy1](https://github.com/jchen9619/Convolutional-Neural-Network-for-Messy-Clean-Room-Detection/blob/main/images/messy/1.png)
 <img src="https://github.com/jchen9619/Convolutional-Neural-Network-for-Messy-Clean-Room-Detection/blob/main/images/messy/1.png" width="150" /> <img src="https://github.com/jchen9619/Convolutional-Neural-Network-for-Messy-Clean-Room-Detection/blob/main/images/messy/12.png" width="150"/> <img src="https://github.com/jchen9619/Convolutional-Neural-Network-for-Messy-Clean-Room-Detection/blob/main/images/messy/19.png" width="150"/> <img src="https://github.com/jchen9619/Convolutional-Neural-Network-for-Messy-Clean-Room-Detection/blob/main/images/messy/4.png" width="150"/> <img src="https://github.com/jchen9619/Convolutional-Neural-Network-for-Messy-Clean-Room-Detection/blob/main/images/messy/7.png" width="150"/> 

**Clean** <br>
<img src="https://github.com/jchen9619/Convolutional-Neural-Network-for-Messy-Clean-Room-Detection/blob/main/images/clean/14.png" width="150" /> <img src="https://github.com/jchen9619/Convolutional-Neural-Network-for-Messy-Clean-Room-Detection/blob/main/images/clean/2.png" width="150"/> <img src="https://github.com/jchen9619/Convolutional-Neural-Network-for-Messy-Clean-Room-Detection/blob/main/images/clean/20.png" width="150"/> <img src="https://github.com/jchen9619/Convolutional-Neural-Network-for-Messy-Clean-Room-Detection/blob/main/images/clean/22.png" width="150"/> <img src="https://github.com/jchen9619/Convolutional-Neural-Network-for-Messy-Clean-Room-Detection/blob/main/images/clean/9.png" width="150"/> 

**Modeling: Neural Network Layers** <br>
In addition to Keras preset model VGG19, the final two Dense layers use Rectified Linear Unit (ReLu) and Sigmoid activation functions after flattening the VGG19 output. Additionally, a callback parameter was included when fitting the model to stop the training process when training accuracy achieved 90%. 

The model summary is as follows: <br>
 
  <img src="https://github.com/jchen9619/Convolutional-Neural-Network-for-Messy-Clean-Room-Detection/blob/main/Files/CNN%20VGG19%20Param.png" width=400 />
  
</p> 

**Conclusion** <br>
Of the 10 test set images, the CNN model successfully predicted the status of 6. Two of the wrong predictions are misleading pictures of messy rooms that can easily be mistaken as clean, as they both show objects with clearly defined edges. 

**Test Dataset Images** <br>


**Prediction Output** <br>
 <img src="https://github.com/jchen9619/Convolutional-Neural-Network-for-Messy-Clean-Room-Detection/blob/main/Files/Model%20Output.png" width=450 />
  
</p> 



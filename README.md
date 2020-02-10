# Neural-Network-Analysis
A brief analysis of the effects of various LR and network architectures on the final Accuracy, Precision, and Recall for model training. The data set used was Flower-17 and the trainging/test divide was around 0.75/0.25.

![FinalStatistics](https://user-images.githubusercontent.com/42900802/74114495-6c19a480-4b78-11ea-860f-f4aa2c103eaa.png)

As you may see in the graph above, the accuracy/presision/recall tend to increase slowly with the learning rate. However after a particular learning rate value, these statistics drop sharply. This threshold can vary depending on the type of architecture used. For example, ShallowNet and MiniVGG have it around $10^{-2}$, but LeNet had it around $10^{-1}$.



 
![Combined_image](https://user-images.githubusercontent.com/42900802/74114481-47253180-4b78-11ea-888d-8f095af4a510.png)

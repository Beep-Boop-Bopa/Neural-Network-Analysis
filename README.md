# Neural-Network-Analysis
A brief analysis of the effects of various LR and network architectures on the final Accuracy, Precision, and Recall for model training. The data set used was Flower-17 and the trainging/test divide was around 0.75/0.25. The models were trained on google collab.

![FinalStatistics](https://user-images.githubusercontent.com/42900802/74114495-6c19a480-4b78-11ea-860f-f4aa2c103eaa.png)

As you may see in the graph above, the accuracy/presision/recall tend to increase slowly with the learning rate. However after a particular learning rate value, these statistics drop sharply giving unsatisfactory performance. This threshold can vary depending on the type of architecture used. For example, ShallowNet and MiniVGG have it around \[10^{-2}\], but LeNet had it around \[10^{-1}\].

The initial increase in these statistics with an increase in learning rate happens because of the SGD algorithm not getting stuck on the local minimas. The sharp decrease happens of the SGD algorithm jumping around too much and not finding the global or near-global minimas. 

## Accuracy/Loss curves 

Another huge reason for such results is over fitting. Please look at the loss/validation curves below.
 
![Combined_image](https://user-images.githubusercontent.com/42900802/74114481-47253180-4b78-11ea-888d-8f095af4a510.png)


## Suggestions for improvements:

1. Repeat the experiment a couple of times for each of the Learning-rate,Model-architecture pairs and take their average. 

2. Try out different training/test divides.

3. Try out other datasets and take averages of the results. 

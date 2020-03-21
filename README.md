# Neural-Network-Analysis
A brief analysis of the effects of various LR and network architectures on the final Accuracy, Precision, and Recall for model training. The data set used was Flower-17 and the trainging/test divide was around 0.75/0.25. The models were trained on google collab. The code for the network architectures was copied from Adrian Rosebrock DL4CV starter bundle. 

## Accuracy/Presision/Recall

![FinalStatistics](https://user-images.githubusercontent.com/42900802/74114495-6c19a480-4b78-11ea-860f-f4aa2c103eaa.png)

As you may see in the graph above, the accuracy/presision/recall tend to increase slowly with the learning rate (LR). However after a particular LR, these statistics drop sharply giving unsatisfactory performance. This threshold can vary depending on the type of architecture used. For example, ShallowNet and MiniVGG have it around 10^-2, but LeNet had it around 10^-1.

The initial increase in these statistics with an increase in LR happens because of the SGD algorithm not getting stuck on the local minimas. The sharp decrease happens of the SGD algorithm jumping around too much and not finding the global or near-global minimas.

Overall, VGGNet gives the best performance if we give it the right LR. ShallowNet seems to have a roughly constant result across different LRs until the LR becomes too big for it. LeNet's increase in these statistics seem to be most significantly affected by increases in LRs.

## Loss/Accuracy curves 

Another huge issue that we need to analyse is over fitting. Please look at the loss/validation curves below.

![Combined_image](https://user-images.githubusercontent.com/42900802/74114481-47253180-4b78-11ea-888d-8f095af4a510.png)

The accuracy curves reach equilibrium at very low percentages (b/w 50%-70%) for all of the architectures for LRs b/w 0.002 and 0.007.

#### MiniVGGNet

An overfit is a situation when the validation-accuracy curves seen below almost reach Accuracy=1.0, but the test-accuracy is turns out to be much lower. MiniVGG seems to be the best example for this. The "yellow" validation-accuracy curve almost hits 1.0 as LR increases, however its test accuracy stops dropping.

#### ShallowNet

Again as said before, ShallowNet seems to be very robust to LRs below a reasonable value, it doesn't seem to overfit. The "yellow" validation-accuracy curve stays constant around 0.6 and the test-accuracy also roughly remains constant.


#### LeNet

For LeNet, the accuracy keeps on increasing for both the validation-accuracy curve and test-accuracy.

#### An observation about noise: 

As the LR increases, the loss/accuracy curves become noisy. This increasing noise can be most significantly observed in the "blue" validation-loss curves. Not saying that the lower the noise the better, but it looks like that as the noise factor gets too high, the accuracy starts dropping. There might be some kind of a correlation between this noise and the overall accuracy. 

## Suggestions for improvements:

1. Repeat the experiment a couple of times for each of the Learning-rate,Model-architecture pairs and take their average. 

2. Try out different training/test divides.

3. Try out other datasets and take averages of the results.

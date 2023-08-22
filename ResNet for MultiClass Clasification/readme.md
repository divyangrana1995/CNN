# Objective:
The objective of this project is to use a dataset of human emotions availble on kaggle to classify the images into its corresponding classes.
# Model used:
I created my own CNN model using the keras Sequential API. Then, I also created a ResNet-34 model from scratch using the subclassing method. 
# ResNet Model:
ResNet Model solves the bottleneck of VGG i.e. limited number of layers in the network. After a certain number of stacked layers in VGG, the performance of the model deteriorates with an increase in depth. Ths is caused by the vanishing gradient problem. When the network is too deep and the gradients in the back layers can produced very small values. While performing chain rule to obtain the gradient for the front layers, the gradients can easily shrink to zero and hence, resulting in the weights never updating its values. This leads to no learning of newer parameters.
ResNet solves this problem by introducing residual blocks that allows skipping connections that can skip layers that contributes a low gradient.Moreover, the ResNet model also introduced the a Batch Normalization layer to deal with internal covariate shift. Thus, increasing the training speed of the model.
# Result:
The result from my custom model showed an accuracy of around 75% on the test dataset. In comparison, ResNet Model showed an improvement in its performance by almost 10%. The ResNet-34 model achieved an accuracy of around 85%. 

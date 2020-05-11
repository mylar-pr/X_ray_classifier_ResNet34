# X-ray image classifier to detect pneumonia 

This project deals with the classification of X-ray images using Deep Learning, into the following classes:
1. Bacterial Pneumonia
2. Normal
3. Viral Pneumonia

Dataset: The data set was acquired from Kaggle. The link to the dataset: https://www.kaggle.com/praveengovi/coronahack-chest-xraydataset
The dataset was segregated into folders with class names with the code present in the notebook for easier training.

Framework used : PyTorch

The images (size:224x224) are trained on a Deep Convolutional Neural Network in a batch size of 16. They are trained in two approaches seperately:
### Approach 1: 
The images were trained on a custom architecture with Cross Entropy Loss and Adam Optimizer. The model was able to classify images with an accuracy of 73.5%.

### Approach 2: 
To get a better accurate model, transfer learning on a more well-proven deep neural network architecture was utilized. 
The problem with approach 1 was caused by vanishing gradients which is a common issue with Deep Neural Networks. For more information: https://en.wikipedia.org/wiki/Vanishing_gradient_problem

This problem was solved by using Residual Networks. For more information on Residual Networks, refer to the ground breaking research paper written by Kaiming He, Xiangyu Zhang, Shaoqing Ren, Jian Sun, from the microsoft research team
https://arxiv.org/pdf/1512.03385

![](https://miro.medium.com/max/1140/1*D0F3UitQ2l5Q0Ak-tjEdJg.png)


By utilizing ResNet34 architecture which was pre-trained on the ImageNet Dataset, a model was trained well enough to classify images with an accuracy of 82.05%

## To run the notebook successfully, download the dataset(the size of the dataset > 1GB) and place it in this folder/repository and run the cells in the notebook.

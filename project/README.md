# Machine Learning
This is the final project of the Machine learning project CS760 in 2020 fall. 

Please see this [link](http://pages.cs.wisc.edu/~zxu444/cs760/) to view code directly.

## Introduction
We applied several machine learning methods on the scanned CT chest images to explore the. relationship between positiveness of COVID-19 and chest CT.
We considered several competitive machine learning approaches, including Logistic Regression, K Nearest Neighbors, Naive Bayes, Decision Tree, Random Forest, Support Vector Machine and Convolutional Neural Network(CNN). We trained these models with raw image data and make predictions. We implemented the transfer learning on our own dataset. We used ResNet-101 architecture and personalized our own fully connection layer at the end. We froze the parameters in previous layers] only trained the personalized layers. In our result, we have SVM achieves the best performance with test accuracy 89%. The ResNet-101 has the second high test accuracy of 81.33%.

To combine the feature extraction advantage of convolutional neural networks and the interpretation of other machine learning methods, we used simple CNN to process images and transfer them into vectors representing the image characteristics. Then we applied several machine learning models to the image features. The advantage of this idea is instead of using raw image pixel value for classification, we implemented our machine learning algorithms on feature vectors extracted by pre-trained Convolutional Neural Network layers. This can reduce the feature dimension significantly, hence reduce the time and space complexity, free up more resources for more analysis. We aim to improve the accuracy of prediction and explore the explanation and interpretation as well.

We make use of the high accuracy from neural networks along with the interpretation from other machine learning models to better help make decisions and explain the relationship between COVID results and scanned images from a different perspective. We hope our model provides some insights into potential applications of machine learning methods in this specific COVID-19 situation.

## Conclusion
We utilize the high accuracy from neural network along with the interpretation from machine learning models to better help make decisions and explain the relationship between COVID results and scanned images from a different perspective.
- SVM is the best model among the selected models to diagnose COVID-19, with the highest test accuracy of 89% and high computation efficiency. The ResNet architecture has the second high test accuracy, which can be improved if we tuned the layers and nodes to make them more suitable for the data.
- The model on raw images works pretty well on the test dataset. However, the models on feature vectors have high train accuracy but lower test accuracy. The main reason is the potential overfitting problem when we fed the extracted features to our model. The CNN extract the main features but neglect some other important factors of the CT images. The focus on minor features may lose the overall characteristics of the images, we need to be careful when we use this idea in image classification.
- In this work, the methods with raw dataset have generally better performance than those on extracted features. In our future work, we can explore more on how to use CNN architecture extract features well and combine them with our other machine learning models.

## Reference
- [package mlxend](http://rasbt.github.io/mlxtend)
- [pytorch](https://pytorch.org)
- [reference in report](https://github.com/OliverXUZY/CS760-ML-fall20/blob/master/project/760project.pdf)



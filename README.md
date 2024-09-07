# Deep Learning Introduction
Deep learning is a branch of machine learning with applications in computer vision, one of which is image classification using the Convolutional Neural Network (CNN) method. CNN architecture consists of 3 layers, namely convolutional layer, pooling layer, and fully connected layer. 

# Background
There are about 400 dog breeds. They are divided into two, ancient and modern. These ancient breeds show the results of early domestication so they still look like wolves and originated more than 500 years ago, while modern breeds represent today's dog breeds with evidence of wolf crossbreeding that can no longer be detected. Ancient breeds are considered to be very similar to wolves compared to modern breeds. (Smith and Van Valkenburgh, 2021).  Breeding can be accomplished through hybridization, which is the process of mixing between different, but adjacent taxonomies that is capable of gene alteration, long-term survival, and evolution. Hybridization is done naturally, but not anthropogenically, by humans either intentionally or for their own purposes.

This process is known as anthropogenic hybridization which often occurs in Canids (Donfrancesco et al. 2019) such as crossbreeding between Siberian Husky, Alaskan Mamute, and German Sheperd dogs with wild wolves resulting in wolfdog hybrids. These breeds are utilized for their health, strength and night vision for military training (Sommese et al. 2021). Hybridization between domesticated species and their ancestors is a threat to the long-term conservation and safety of a species. The presence of gene-mixed individuals in a population can make the distinction between them ambiguous (Pilot et al., 2018).

#Purpose
The purpose is to create a model that is able to classify images of dogs and wolves that are expected to help the public in knowing the differences between the two species as well as rescuers and those who have a desire to keep them in order to facilitate identification.

#Scope
The research dataset was obtained through Kaggle which can be accessed at the link https://www.kaggle.com/datasets/harishvutukuri/dogs-vs-wolves. The data was processed by downloading and then saving it using Google Drive media. The data amounted to 2000 images which were divided into two subfolders, namely dogs and wolves, each of which amounted to 1000. The data on Google Drive is then connected to Google Colab for preprocessing. Furthermore, the data is divided into training and test with a ratio of 80:20 for the training and testing process. Training data will be trained on the model then test data is used for model validation which from both data will be obtained accuracy to find out how well the model classifies dog and wolf images.

![image](https://github.com/user-attachments/assets/b2214060-5d4e-48ff-afc8-d757bfef3209)


# Deep Learning Model
The model used pre-trained weight from ImageNet and CNN architecture Xception. It was trained in 2 x 15 epoch, the first 15 is for transfer learning and the other 15 is for fine-tuning. The model then evaluated using confusion matrix and classificiation reports, this include precision, recall, F1-score, and accuracy. The data is balanced with 1600 for training and 400 for testing.

# Why use pre-trained?
Traditional CNN models have shortcomings in the field of pattern recognition, especially RGB images where the mulltilayer perceptron (MLP) has limitations especially in processing an image. For each input, MLP will use one perceptron which in the case of RGB images each pixel will be multiplied by three because there are three channels in RGB. The weights used in each perceptron will increase significantly in large images and make the model unable to manage the weights perfectly which will cause overfitting and difficult training. Transfer learning (TL) can be utilized in reducing overfitting, where the model learns a problem that is then used as a starting point for other tasks. Transfer learning uses feature extraction techniques from pre-trained models and TL is generally trained with large datasets such as ImageNet and the parameters obtained from model training results can be used for custom artificial neural networks (Salehi et al., 2023).

# Conlusion and Suggestions
The training was done using 2 x 10 epoch and patience of early stopping to 5, the fine-tuning managed to get an overall accuracy of 73%. The confusion matrix shows that the model can classify wolves better than dogs with 82 images of dogs falsely predicted as wolves.

![image](https://github.com/user-attachments/assets/e2c5839d-2d68-4a14-892b-8fa41ef9d755)

Classification in dog and wolf images has shortcomings in limited datasets and more diverse data is needed to increase the accuracy of the model. Data limitations are prone to model overfitting which has been slowed down by applying augmentation and regularization to enlarge the dataset, it is hoped that new data can be obtained so that it can help the model in the learning process to perform classification with a higher level of accuracy.





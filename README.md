## Autoencoder for Credit-Card-Fraud-Detection

### Overview
### Anomaly Detection With Autoencoders
**The accuracy of a classifier model directly depends on how esily distigushable the data is. The more abstract the data is more easy it is for the model to classify. The **Autoencoders** helps us to do the exact same. The Autoencoder can help us create lower dimensional representation of the data distribution. This latent representation of original data is more distinct than the original thus can be easily distinguished by a classifier model.**

### Insight
We are going to train an AutoEncoder for Credit Card fraud Detection and get a latent space representation of data and use that data to train a classifier model.

The data distribution can be visualised using **UMAP** which is a dimension reduction technique.
Dimensionality reduction is a technique which is used for creating lower dimensional data while keeping its inherent structure. 
This helps for visualization of data with large number of features in a 2-d space.
You can install umap by
```
pip install umap-learn
```
### Result

Below is the visulization of the data distribution before and after feeding through the encoder. We can clearly see that the data is now more abtract than before.

![Screenshot 2024-01-03 090806](https://github.com/mishra-18/Credit-Card-Fraud-Detection/assets/155224614/19cf9c19-3fdd-47e6-9080-e34969b5f427)

## Autoencoder Architecture

<img width="850" alt="autoencoder-architecture" src="https://github.com/mishra-18/Credit-Card-Fraud-Detection/assets/155224614/5896b5f8-ff96-43ca-8295-1293def63d7b">

The autoencoders is trained with unsupervised learning, an autoencoder does not have any target data but rather uses the same input as target. It first reduces the dimension to a latent space and then decodes the vector to the original input shape. It evovels through reducing the loss and reproduce the input data.
Here we aim to feed the data to a trained autoencoder and extract the new data representation. Later we can perform supervised learning classification task on the new data representation.

An autoencoder consists of and encoder, latent space, and a decoder. The encoder layer compreses the input data to a latent space and the decoder layer decodes and uncompresses the data and reproduces the original data. We are goning to train this model for the entire data according to train_test_split and visualize the new latent representation of our data.

Here we aim to feed the data to a trained autoencoder and extract the new data representation. Later we can perform supervised learning classification task on the new data representation.

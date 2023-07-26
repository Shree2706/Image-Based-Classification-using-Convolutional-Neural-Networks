# Image-based-Classification-using-Convolutional-Neural-Networks
It is a Deep Learning Project based on CNN predicting the name of the object by its image. Uisng the CIFAR-10 dataset.
In the CIFAR-10 dataset, there are 60,000 images of objects and creatures derived as classes in the notebook, such as Airplane, Automobile, Horse, Birds, Cat, Deer, Dog, Frog, ship, Truck. 
There are total 10 classes and each class has 6000 images in different natural and lightng conditions. All of 32*32 px.

Here, in this project the very first thing to do is to download the CIFAR-10 dataset, since it is already present in 'tensorflow.keras' module of tensorflow.

Then after train, test split in the dataset, first built an Artificial Neural Network(ANN) model to be curious to compare the accuracy score with the Convolutional Neural Network(CNN).

So, in the ANN, add four layers, one Flatten layer and three Dense layer, with the activation function 'relu' iin the first three layers, and a 'softmax' function in the last layer, and in the end compile it with the Stochastic gradient descent (SGD) optimizer, and loss function of 'sparse_categorical_entropy', at the epochs value of 5. After training the model we get the accuracy of '0.4964', and loss of '1.4311'

After the ANN model, we plotted the confusion matrix on the basis of the predictions made by the ANN model.

Now, started building the Convolutional Neural Network (CNN) model.
For that the layers added are in batches, in the first batch we add a conv2D layer and a max pooling2D layer of (2,2), with 32 filters, kernal size of (3,3), input shape of (32,32,3) and activation function 'relu'.

And in the second batch again add a conv2D layer and a max pooling2D layer of (2,2), but this time with 64 filters, kernal size of (3,3), and activation function 'relu'.

And then n the last batch we add our flatten layer and two dense layers with activation function of 'relu' and 'softmax' respectively.

When the model gets trained, compile it by using the optimizer 'adam', and los function of 'sparse_categorical_entropy', and finally train the model with epochs value of 10. 

We get the accuracy of '0.8031', and loss of '0.5597'

And for model to predict the class of the image, calculate the 'y_pred' score.


# Human Facial Expression Recognition
A CNN based approach to recognize and classify the human facial expressions from images

# 1. Introduction
A Convolutional Neural Network (ConvNet/CNN) is a Deep Learning algorithm which can take in an input image,assign importance (learnable weights and biases) to various aspects/objects in the image and be able to differentiate one from the other. I used the convolutional neural network in order to identify the emotion in the images and classify the images accordingly.

# 2. Data
The input data from the dataset was in string format. The contents of this string a space-separated pixel values in row major order. In order to train the cnn on the input data, the string format was converted into 48x48 size array which contained the information of the image pixels.The dataset contains two columns (emotion and pixels) as shown in the table below and the labels that were assigned to each emotion is depicted in the table. The bar graph denotes the frequency of each emotion occurring in the dataset.

![Screenshot from 2021-03-16 16-01-00](https://user-images.githubusercontent.com/17639991/111295045-f2a08f80-8670-11eb-85a1-631fe45de1cc.png)

![Screenshot from 2021-03-16 16-01-50](https://user-images.githubusercontent.com/17639991/111295103-051ac900-8671-11eb-98d8-069d2cf1d482.png)

# 3. Data Augmentation
Data Augmentation is a technique that is used to artificially expand the size of training data set by creating modified
images of images already present in our dataset. Modified images were produced by zooming, rotating, translating and shearing the existing images. This technique works because modifying images using these transformations doesn’t change the label associated with them. Image Data Generator class from Keras library in Python was used for data augmentation.

# 4. Results and Analysis

![Screenshot from 2021-03-16 16-11-03](https://user-images.githubusercontent.com/17639991/111296324-5bd4d280-8672-11eb-9d93-f75ed05e8c5f.png)
![Screenshot from 2021-03-16 16-11-16](https://user-images.githubusercontent.com/17639991/111296329-5d05ff80-8672-11eb-89f0-80e5d76b8dec.png)

The accuracy increases with the increase in number of epochs as the model is trained and reaches its peak accuracy ie. 0.675408
Validation accuracy: 0.675408
Training set accuracy: 0.825110

# Dog Breed Identification
##### Classifying images of 120 dog breeds using Xception Model

## Evaluation Metric
This competition evaluates the model predictions on the test set on **Multi Class Log Loss**.
The final score of this model was **0.94762**

## Data
The data can be found in this [Kaggle competition](https://www.kaggle.com/competitions/dog-breed-identification). 
&nbsp;

It consists of 10,222 training and 10,357 testing images from 120 different dog breeds.
Data augmentation and nomralization is performed using the `ImageDataGenerator`. 
&nbsp;
Also the data is skewed so some upsampling would be benfitial.


## Model
Transfer learning is used. The **Inception** and **Res-Net** architectures were tested but the **Xception** outperformed both of them.
&nbsp;
The model was pretrained on the **imagenet** dataset. A small calssifier is connected to the model which was trained firstly while freezing the weights of the Xception model. Then the weights were unfreezed and the whole model was trained

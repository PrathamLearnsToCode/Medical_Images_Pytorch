# Medical_Images_Pytorch

Pneumonia Segmentation:
It's a common infectious disease which can be life threatning if not diagnosed in time. The dataset used to train the model is imported from RSNA pneumonia detection Challenge containing 26684 X-Ray Images. Link to the dataset: https://www.kaggle.com/competitions/rsna-pneumonia-detection-challenge/data.

Steps taken for pre-processing the raw data->
1. Resizing of original 1024 dimensional images into 224 dimensions to make it computationally less expensive
2. Standardizing each pixel value in the interval of [0,1] by dividing it by /255.
3. Splitting the dataset into 24000 train images and2684 test images
4. categorical encoding to our predicition as: 0 if no pneumonia detected, 1 if pneumonia detected

Network Architecture Used:
ResNet 18

Loss Function: 
BCEWithLogitsLoss

Optimizer:
Adam with learning rate 1e-4

Epochs for training:
30



Cardiac Detection:
It indicates size and position of the heart. Cardiomyopathy which is disease of the cardiac muscle which midght lead to heart failure or blood clots often comes with the size of the heart. Pneumorothox and Atelctasis which both leads to collapse of the lungs are sometimes accompanied by a change in position of the heart. Therefore, early detection reduces the risk and long term consequences. The dataset used to train the model is imported from RSNA pneumonia detection challenge containing 496 X-Ray Images. Link - https://www.kaggle.com/competitions/rsna-pneumonia-detection-challenge/data.

jfijicih

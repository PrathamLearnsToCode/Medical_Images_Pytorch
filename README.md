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



Atrium Segmentation:
Segmenting an image is the process of assigning a specific class to all pixels or voxels in an image. Each voxel is either classified as not left atrium or left atrium. The segmentation of the atrium allows to exactly calculate its volume. Changes in atrial volume are associated with cardiac disorders, such as atrial fabrillation or mitral valve stenosis(narrowing of the mitral valve orfice, blocking blood flow). Link to the dataset: http://medicaldecathlon.com/.
General Description of Data:
1. 20 MRI scans of heart with corresponding ground truth mask
2. 4542 2D MRI and label slices

Steps taken for pre-processing the raw data->
1. Extracting slices from 3D MRI data
2. Crop away non cardiac regions and background(on segmentation masks too)
3. Z-normalization oer subject
4. Standardize the normalized subject into the interval [0,1]
5. Use 16 patients as training data and the remaining 4 for validation


Task:
1.Create a list of all 2D slices
2.Extract and load slice coreesponding label mask
3.Data augmentation
4.Return a augmented slice and mask

Network Architecture Used:
U-Net

Loss Function: 
Dice Loss

Optimizer:
Adam 

Epochs for training:
75

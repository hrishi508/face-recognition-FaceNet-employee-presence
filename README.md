An implementation of the paper - "Face Recognition System using Facenet Algorithm for Employee Presence" by Ferry Cahyono  et al., 2020.

# Versions
1) Python     - 3.8
2) Tensorflow - 2.5.0
3) Keras      - 2.4.3 

# Data Description
1) FERET - https://www.nist.gov/itl/products-and-services/color-feret-database
2) Georgia Tech Face Database - http://www.anefian.com/research/face_reco.htm
3) KomNET Face Dataset - https://data.mendeley.com/datasets/hsv83m5zbb/2 
## Train/Test split
### FERET   
    subjects     -  111  
    total images - 1443 (13 per subject)  
    train images - 1110 (10 per subject)  
    test  images -  333 ( 3 per subject)  
### Georgia Tech Face Database    
    subjects     -   48  
    total images -  624 (13 per subject)  
    train images -  480 (10 per subject)  
    test  images -  144 ( 3 per subject)
### KomNET Face Dataset    
    subjects     -   50  
    total images -  650 (13 per subject)  
    train images -  500 (10 per subject)  
    test  images -  150 ( 3 per subject)
From all the images in the above dataset, cropped face images were extracted using the Multi-task Cascaded Convolutional Networks (MTCNN) package in Keras.  
'Sample Data' consists of the first ten subjects of the created dataset.
    
# Architecture
FaceNet was used to obtain feature vectors of the face images followed by Support Vector Machine (SVM) to classify the feature vectors by subjects.  
FaceNet weights can be obtained here: https://github.com/nyoki-mtl/keras-facenet

# Results
An classification accuracy of 100% was obtained on the dataset of 209 subjects.
Given below is the visualization of the 2D feature vectors obtained by performing PCA analysis on the FaceNet outputs of 'Sample Data' train images.  
  
![WhatsApp Image 2021-08-23 at 7 05 23 PM](https://user-images.githubusercontent.com/68325029/130456700-d44280e1-046e-47f8-9a4e-cb5cba832c54.jpeg)

# References
1. F. Cahyono, W. Wirawan and R. Fuad Rachmadi, "Face Recognition System using Facenet Algorithm for Employee Presence," 2020 4th International Conference on Vocational Education and Training (ICOVET), 2020, pp. 57-62, doi: 10.1109/ICOVET50258.2020.9229888.
2. https://github.com/nyoki-mtl/keras-facenet
3. Astawa, I Nyoman Gede Arya (2020), “KomNET: Face Image Dataset from Various Media”, Mendeley Data, V2, doi: 10.17632/hsv83m5zbb.2

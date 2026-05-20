Name : Priscilla Tiara S 

Student Number : 4222301026

Class : RE 6 A

# COMPUTER VISION (MIDTERM TASK) 
Image Classification with Machine Learning

Dataset : 
eminist-letters-train.csv
Original size: 88,800 samples, 26 classes (A–Z)
Used in this project: 2,600 samples — 100 per class (balanced)

Inside this notebook, the program starts by reading the emnist-letters-train.csv file and fixing the image orientation since EMNIST stores images rotated and flipped by default. After that, it takes exactly 100 samples per class (26 classes × 100 = 2,600 total) and shuffles the entire dataset before processing. The images are then visualized to make sure everything looks correct, followed by HOG feature extraction which converts each 28×28 image into 1,296 numerical features representing the shape and edges of each letter. The dataset is then split 80% for training and 20% for testing, with StandardScaler applied to normalize the feature values. Next, Grid Search automatically tries 12 combinations of SVM parameters (kernel, C, gamma) using 5-Fold Cross Validation to find the best configuration. Finally, the best model is evaluated using LOOCV and tested on the test set, reporting accuracy, precision, recall, and F1-score, along with a confusion matrix heatmap that shows which letters are most commonly misclassified.

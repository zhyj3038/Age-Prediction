                                              Age-Prediction 
This project is based on the dataset provided by wiki/Dataset

link:-"https://data.vision.ee.ethz.ch/cvl/rrothe/imdb-wiki/"

# Machine Learning
Machine learning is a field of computer science that gives computers the ability to learn without being explicitly programmed. The name Machine learning was coined in 1959 by Arthur Samuel

# Regression
In statistical modeling, regression analysis is a set of statistical processes for estimating the relationships among variables.

 Regression analysis is a form of predictive modelling technique which investigates the relationship between a dependent (target) and independent variable (s) (predictor). This technique is used for forecasting, time series modelling and finding the causal effect relationship between the variables.

# Computer Vision
Computer vision tasks include methods for acquiring, processing, analyzing and understanding digital images, and extraction of high-dimensional data from the real world in order to produce numerical or symbolic information, e.g., in the forms of decisions.

# Project Structure
     1:- OVERVIEW
     2:- WORKING
     3:- REQUIREMENTS
     4:- INSTALLATION
     5:- DATASET SANPSHOT
     6:- DATA PLOTTING and GRAPHS
     7:- PREDICTION
     8:- GENDER ANALYSIS AND LEARNING CURVE
     9:- OBJECT DISTANCE CALCULATION
     10:- OUTPUT

# Overview
This Project is an application based on Computer vision and Machine learning implementation using regression supervised classification.
# Working
![alt_tag](https://github.com/vshantam/Age-Prediction/blob/master/Analysis/working.png)


# Requirements
     1:- SCIKIT-LEARN
     2:- PICKLE
     3:- MATPLOTLIB
     4:- NUMPY
     5:- PANDAS
     6:- OS/SYS
     7:- CV2
     
# Installation
Suggested to use Python3 pip version i.e pip3 to install packages.

if you do not have pip3 installed in your system .

Use this command:

     sudo apt-get install python3-pip --upgrade # for pip3
     sudo apt-get install python-pip --upgrade #for pip 
eg:-

     pip3 install scikit-learn #for sklearn 
     
# Dataset Snapshot
Features set                 
![alt_tag](https://github.com/vshantam/Age-Prediction/blob/master/Analysis/Screenshot%20(20).png)
Output set                   
![alt_tag](https://github.com/vshantam/Age-Prediction/blob/master/Analysis/Screenshot%20(21).png)

# Data Plotting and Graphs
Histogram plotting                                                                                                     
![alt_tag](https://github.com/vshantam/Age-Prediction/blob/master/Analysis/Figure_3.png)

Plot variation                                                                                                        
![alt_tag](https://github.com/vshantam/Age-Prediction/blob/master/Analysis/Figure_2.png)

Pie chart Analysis                                                                                                           
![alt_tag](https://github.com/vshantam/Age-Prediction/blob/master/Analysis/Figure_1.png)

Combination of simple plot and Histogram                                                                                        
![alt_tag](https://github.com/vshantam/Age-Prediction/blob/master/Analysis/Figure_4.png)

# Predictions
This is a real time application using webcam feed so the accuracy will not be much reliable but close to the actual values.One can expect variatons also.

The reason could be anythng Like :
                            
    Quality of the images
    Noise in the Image
    Fps Distribution
    
The application Predicts only when the Face is been detected by the camera in Real Time.If it fails to predict the face then it Halts until it finds one..

scripts :-

      $ python3  Dataset.py
The wiki datset folder structure looks like                     
![alt_tag](https://github.com/vshantam/Age-Prediction/blob/master/Analysis/Capture.PNG)

where each folder contains images of peaple which age labled on the image
this function hels to loop through all the folder images and scales them,after that the script puts the all images into the sample images folder                               

![alt_tag](https://github.com/vshantam/Age-Prediction/blob/master/Analysis/Capture1.PNG)


    $ python3 cropfunc.py
This function helps to loop through all the resized image and detect the faces in it . if the face is been detected then it crops the facial par and saves it in the sample cropped folder.

![alt_tag](https://github.com/vshantam/Age-Prediction/blob/master/Analysis/Capture2.PNG)

After the crop procedure script provide function to convert the color images into grayscale image.
![alt-tag](https://github.com/vshantam/Age-Prediction/blob/master/Analysis/Capture3.PNG)

    $ python3 clf.py
 This functon is used for loading the dataset and classifier using machine learning modules.
 
 The classifier can be saved using pickle module if you are usng scikit learn and the formats are:
 
    1:- sav
    2:- pkl
    
 if you are using Deep Learning Modules such as keras,Tensorflow you can use the Following formats:

    1:- hdf5
    2:- h5py
    3:- YAML
    4:- JSON

 
 # Gender Analysis  and Learning Curve
 
                                        Training Set         
                                                                                         X-axis : Accuracy
                                                                                         Y-axis : Loss
 
 
 Simple Plot                                                            
 ![alt_tag](https://github.com/vshantam/Age-Prediction/blob/master/Gender/gplot1.png)
 
 
   
 Scatter Plot                                                                                    
 ![alt_tag](https://github.com/vshantam/Age-Prediction/blob/master/Gender/gplot2.png)
 
 
 
 Pie Chart                                                   
 ![alt_tag](https://github.com/vshantam/Age-Prediction/blob/master/Gender/gplot3.png)
 
                                         Testing set
                                                                                              X-axis : Accuracy
                                                                                              Y-axis : Loss
                                         
 
 Simple Plot                                              
 ![alt_tag](https://github.com/vshantam/Age-Prediction/blob/master/Gender/gplot4.png)
 
 
 
 Scatter Plot                                            
 ![alt_tag](https://github.com/vshantam/Age-Prediction/blob/master/Gender/gplot5.png)
 
  
  
 Pie Chart                              
 ![alt_tag](https://github.com/vshantam/Age-Prediction/blob/master/Gender/gplot6.png)

# Object Distance Calculation

In order to determine the distance from our camera to a known object or marker, we are going to utilize triangle similarity.

we have a marker or object with a known width W. We then place this marker some distance D from our camera. We take a picture of our object using our camera and then measure the apparent width in pixels P. This allows us to derive the perceived focal length F of our camera:

                F = (P x  D) / W
                
 I can apply the triangle similarity to determine the distance of the object to the camera:

                D = (W x F) / P
                
Here "D" is the Actual Distance alculated by the system and "F" is the Focal length calculated by the system.

For references use the link : ("https://stackoverflow.com/questions/14038002/opencv-how-to-calculate-distance-between-camera-and-object-using-image")

# Output

Does the Actual Prediction

      $ main.py
    
Output 1:

    Predicted Age :- 24
    Actual Age :- 21
![alt_tag](https://github.com/vshantam/Age-Prediction/blob/master/Analysis/output4.gif)

Output 2:
![alt_tag](https://github.com/vshantam/Age-Prediction/blob/master/Analysis/output2.gif)

Output 3:
![alt_tag](https://github.com/vshantam/Age-Prediction/blob/master/Analysis/output3.gif)
 

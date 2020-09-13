# Intrusion-Detection-System

# Link to App:
https://btp-intrusion-detection.herokuapp.com/

It is our thesis project in which we developed an intrusion detection system and integrated it
with web application.This system classifies the traffic of a site as a normal traffic or a type of attack like DOS
attack,probe attack, teardrop attack.

### DOS Attack
In dos attack intruder sends large no. of requests on a server and exhausts all the
resources of the server so that legitimate users can't access the server.
### PROBE Attack
In this attack Intruder tries to gain access to the information and loopholes in the
system and later use this information for generating the attack.
### Teardrop Attack
In tear drop attack intruder modifies the requests packet.it modifies the sequence no. of request packets so it creates the problem in reassembling of the packets at
receiver and buffer is full and all other incoming packets are discarded.


## we divided this project into 4 phases:

### First Phase:
We use KDD-99 dataset which consists of different features related to traffic data of a site and
one target field.
Target field has 4 categories of values: normal traffic,DOs Attack,Probe Attack and TearDrop
Attack.
First of all we train base learners like decision tree, KNN, and Naive bayes classifiers.(60% for
training) and found that decision tree is giving the highest accuracy.(89%).

### Second Phase:
We use ensemble approaches Bagging and Boosting:
<------------Ensembling------------->
Ensemble approach combines different machine learning models together in order to better
classify the data.
Bagging, Boosting.
### <---------------Bagging----------->
In bagging, we create bootstrap samples randomly from the given dataset and build a
classifier with each sample.
and after that we combine the result of all the classifiers to classify the data.
### <---------------Boosting------------>
Boosting is a sequential learning algorithm which converts weak learners into strong learners.
In each iteration it increases the weights of those tuples which are poorly predicted in the last
iteration.This process goes on until we find the model which classifies all the tuples correctly.
From bagging we achieved 90.6% accuracy and boosting we found 91% accuracy

### Third phase:
Our proposed work was mainly focused on this technique.
We use a mixture of expert technique.
in this part first we found the accuracy of individual base learners for each type of attack
Means which base learner is giving highest accuracy which type of attack.
Like we assign the weights to each base learner corresponding to each attack.
In mixture of experts different classifiers classify the tuple with attack with the probability
So the result of the classifier with the highest probability will be assigned as the final result.
If for each prediction probability is same then we will multiply this probability with corresponding
weight which is previously calculated. Now the maximum value of this multiplication will be the
final result.
 #### We acheived 95.6% of accuracy with this technique.
 
 ### Fourth phase:
Finally we integrate this mixture of expert models with web application.
For integration we use Flask which is a python framework,and for frontend we used HTML CSS BOOTSTRAP.

## Future Work
Our future work is to develop an intrusion detection system that dynamically detects the
attacks on a website.

# ScreenShots of Website:

# Home Page
![ScreenShot](https://github.com/gangwar-107/Intrusion-Detection-System/blob/master/Screenshot%20(237).png)

# Project Description 
![ScreenShot](https://github.com/gangwar-107/Intrusion-Detection-System/blob/master/Screenshot%20(238).png)

# Dataset Description Page
![ScreenShot](https://github.com/gangwar-107/Intrusion-Detection-System/blob/master/Screenshot%20(239).png)

# Ml Model Page
![ScreenShot](https://github.com/gangwar-107/Intrusion-Detection-System/blob/master/Screenshot%20(240).png)



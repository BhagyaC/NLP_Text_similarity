It is an implementation of gradient boosted decision trees designed for speed and performance
# Why is boosting used
- Inorder to solve convolution and complex problems
- Consider the problem of solving the cat and dog images
- There are many learnrers like cat eye which indicate a cal and long limbs indicate a dog
- But we can't rely on these parameters only in that case we take a weighted average of all of them 
- These rules help us identify whether an image is a dog or a cat but if we were to classify an image based on an indivitual the prediction would be flawed
- Ecah of these rule indivitually are called weak learners becuase these rules are not strong enough to make predictions
- It will combine the all weak learners to a strong learner inorder to give a better model

# What is boosting
- Boosting is a process (ensemble learning technique) that uses a set of machine learning algorithms to combine weak learner to form strong learners inorder to increase the accuracy of the model
## What is ensemble learning
- Ensemble learning is a method that is used to enhance the performance of machine learning model by combining several learners
- When compared to a single model, this type of learning builds with improved efficiency and accuracy
- Bagging in a parallel techinque where boosting is a sequential technique
- In boosting the weak learner are sequentially produced during training
- The perforamnce of the model is improved by assigning a higher wieghtage to the  are previously incorrectly classified samples - adaptive boosting algorithm
- feed the entire data set to the algorithm and the algorithm will make some predictions
- Let the algorithm miss classifies some of the data
- Then pay attention to the miss classified data points
- Improve the weightage and giving lot more importance to the value
- Keep doing this until all the miss classified samples are correctly predicted
- The parallel ensemble learning also known as bagging
- The weak learners are produced parallely during the training phase
- the performance of the model can be increased by parellely training the learners on the boostarp data set - an example is random forest learning
- divinding the dataset to bootstrap data set and running the weak learners on the all dataset
# How the boosting algorithm works
- Basic principle is that generate multiple weak learners and combine them to a one strong rule
- these weak learners are generated using base machine learning algorithms on the different distributions of the dataset
- The basic algorithms are decision trees by default in the boosting algorithms
- The algorithm generate weak learners for each iterations
- After multiple iterations they become a strong learner and give a accurate out come
- The all datapoints in the algorithm is given the same weightage
- on each iteration it will create a different decision boundary and at last all the decision boundaries are combined to make a strong classifier
- After the first iteration it will focus on the miss classified datas and give more weights to them and it will make sure that the next iteration the misclassified data are classified correctly

# Types of boosting
## Adaptive boosting
- each obeservation is weighted equelly for the first decision stump
- Draw out a decision stump in first iteration
- The misclassified outputs are assigned higher weights
- After that new decision stump is drawn by considering the obs. with higher weights as more significant
- Again if any obs are misclassified they're given higher weights
- these steps will be looped until all datapoints are classified to right class - can be used in regression as well but common in classification problems
## Gradient boosting
- In gradient boosting base learner are generated sequentially in such a way that the present base learner is always more effective than the previous one
- The basic differents is that the weights for the missclassified items are not incremented
- Instead it try to optimize the loss fuction of the previous learner it add the weak learner inorder to reduce the loss fuction
- it has three component
- 1. Loss function that needs to be ameliorated
- 2. weak learner are  needed for computing predicion and forming strong learner
- 3. An additive model that will regularize the loss function - try to fix the error or the loss from the previous weak learner
- It can be used for both regression and classification problems
## XGBOOST
- It is an advanced version of gradient boosting method that is designed to focus on computational speed and model efficiency 
- It is introduced becuase the gradient boosting algorithm is computed in a slow rate because of the sequential analysis of the data set
- It supports parallalization by creating decision trees parallely
- It introduces something called distributed for large and complex module
- It uses out- of- core computing inorder to anlyse the huge and varied dataset
- It used cache optimization

- 

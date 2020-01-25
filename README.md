# Datathon2020

Powerpoint slides: https://docs.google.com/presentation/d/1b2iTztlc7klnzxOOxwGk6fqruVa9xCwgwMD7EabDb34/edit?usp=sharing

This Datathon2020 project by Brandon and Irpan focuses on trying to predict divorces given a set of questionnaire answers.  We utilize an artificial neural network with two dense layers to output a decimal between 0.5 and 1.  This decimal is representative of how likely a divorce will happen.  In general, any values exceeding 0.75 indicates a divorce in the immediate future.  Any values below indicates that the couple will be suriving.  In this way, we are able to convert the problem from a regression problem back into a classification problem.  

The external libraries we used are called "Tensor" (not TensorFlow), from the MyGrad folders created by Ryan Soklaski.  I am unable to upload the entire library but our jupyter notebook makes extensive use of this Tensor library. 

To determine the learning rate and regularization values, we used 5-fold cross validation to tune these hyperparameters.  After repeated iterations and several scatter plots created (whch are displayed in the jupyter notebook), we discovered that when the learning rate 
= 1e-7 and the regularization rate = 1e3, our model is the most effective.  

To keep track of the progress of the model's progress, we use the mean squared error.  As the model progresses, ideally, the MSE should drop.  Additionally, to help the model develop, we utilize two activation functions, relu and sigmoid, and use one loss function, the cross entropy loss.  All of which were specifically picked because of the nature of the problem.  The progression of the loss function and the MSE as the model trained are displayed in graphs in the notebook.    

When the model has concluded running, we are able to discern which questions were especially important in the decision to divorce and stay married.  By looking at the magnitude of the calculated weights, we were able to keep track of which questions had larger magnitude weights, allowing us to compile a list of questions that were pivotal and crucial in relationships.  This is intuitive, as the smaller the magnitude of weight, the less the actual question will affect the final decision (in the case of dense layers and linear classifiers).  

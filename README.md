# Datathon2020

This Datathon2020 project by Brandon and Irpan focuses on trying to predict divorces given a set of questionnaire answers.  We utilize an artificial neural network with two dense layers to output a decimal between 0.5 and 1.  This decimal is representative of how likely a divorce will happen.  In general, any values exceeding 0.75 indicates a divorce in the immediate future.  Any values below indicates that the couple will be suriving.  

The external libraries we used are called "Tensor" (not TensorFlow), from the MyGrad folders created by Ryan Soklaski.  I am unable to upload the entire library but our jupyter notebook makes extensive use of this Tensor library.  

We utilize two activation functions, relu and sigmoid, and use one loss function, the cross entropy loss. 

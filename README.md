# Neural Network Charity Analysis

## Overview of the Project
The goal of this project was to create a neural network model that accurately predicts if an organization is a good recipient of donations from a hypothetical philanthropic foundation, AlphabetSoup.  The neural network we ultimately created involved a .csv file that we were given that included approximately 34,000 rows of data about different organizations.  Upon downloading this data, our initial task was to prepare the data so that it could be inputted into a neural network.  This required us to drop and bin unnecessary columns, encode the values of the categorical columns, and standardize the dataset.  Once this was done, we split our prepared data into training and testing sets, and passed these training and testing sets into our neural network model.  Ideally, we hoped to have generated a neural network model that predicted, with at least 75% accuracy, which organizations would be the best for AlphabetSoup to donate to.  However, as described below, we see that we were unsuccessful despite numerous attempts.  We conclude this project description with a summary of our results, as well as other ways we could have attempted to create a more accurate model.     

## Results
As mentioned above, we created several deep neural networks that were able to predict which organizations would be good candidates for donations from AlphabetSoup.  As part of the preparation of our data, we had to determine which column(s) would be included as features and which column(s) would be included as the target for our neural network models.  After dropping unnecessary columns that were not beneficial to the creation of our neural network models, namely the “EIN” and “NAMES” columns, it was decided that the “IS_SUCCESSFUL” column would be the target variable and every other column would be used as the features for our neural network models.    The following bulleted list goes through the design specifications of each neural network.  (It is to be noted that every neural network listed below was compiled using the ‘binary_crossentropy’ loss function and the ‘adam’ optimizer, and all of these neural networks were run for 100 epochs.)

* As shown in the pictures below, the first neural network we created consisted of an input layer, one hidden layer, and an output layer.  The input layer consisted of 80 neurons and used the ReLU activation function.  The hidden layer consisted of 30 neurons and also used the ReLU activation function.  Finally, the output layer consisted of one output neuron and used the sigmoid activation function.  The structure of these layers resulted in a total of 5,981 trainable parameters.  Overall, this neural network produced a loss of approximately 0.5709 and an accuracy of approximately 0.7250 (or 72.50%).  

![Mod20_OriginalNNStructure](https://user-images.githubusercontent.com/115128743/224512007-2811dccf-a260-4a62-b66c-79ae3ec3f153.png)

![Mod20_OriginalNNEvaluation](https://user-images.githubusercontent.com/115128743/224512010-fff34bce-afe5-4e96-aec6-f6b6b465dcda.png)



* As shown in the pictures below, the second neural network we created also consisted of an input layer, one hidden layer, and an output layer.  As before, the input layer consisted of 80 neurons and used the ReLU activation function.  However, for this model, the hidden layer consisted of 40 neurons and used the ReLU activation function.  This increase in neurons was done to hopefully increase the model’s accuracy, as there would be more neurons to determine relationships in the data.  Finally, the output layer consisted of one output neuron and again used the sigmoid activation function.  The structure of these layers resulted in a total of 6,801 trainable parameters.  Overall, this neural network produced a loss of approximately 0.5613 and an accuracy of approximately 0.7254 (or 72.54%).  

![Mod20_1stAttempt_NNStructure](https://user-images.githubusercontent.com/115128743/224512029-e8ac1eb1-4bb4-406e-8281-d4af84dfb674.png)

![Mod20_1stAttemptEvaluation](https://user-images.githubusercontent.com/115128743/224512032-c9acc73c-9577-4a5b-ad29-955f13695de1.png)



* As shown in the pictures below, the third neural network we created again consisted of an input layer, one hidden layer, and an output layer.  The difference between this neural network and the previous two networks lies in the activation functions used in each layer.  The change in the activation functions was done to hopefully help the model make better predictions with the relationships present in the original data.  The input layer consisted of 80 neurons and used the sigmoid activation function.  The hidden layer consisted of 30 neurons and used the tanh activation function.  Finally, the output layer consisted of one output neuron and used the sigmoid activation function.  The structure of these layers resulted in a total of 5,981 trainable parameters.  Overall, this neural network produced a loss of approximately 0.5581 and an accuracy of approximately 0.7255 (or 72.55%).  

![Mod20_2ndAttempt_NNStructure](https://user-images.githubusercontent.com/115128743/224512050-f62937f4-fa7a-4ec0-aea4-17a0040691dd.png)

![Mod20_2ndAttemptEvaluation](https://user-images.githubusercontent.com/115128743/224512051-d2cfa32c-866b-46f3-adfa-06198d0c1bd6.png)



* As shown in the pictures below, the fourth and final neural network we created consisted of an input layer, two hidden layers, and an output layer.  The difference between this network and the prior three networks is that there are now two hidden layers instead of just one.  The input layer consisted of 80 neurons and used the ReLU activation function.  The first hidden layer consisted of 40 neurons and also used the ReLU activation function.  The second hidden layer consisted of 10 neurons and used the ReLU activation function.  Finally, the output layer consisted of one output neuron and used the sigmoid activation function.  The structure of these layers resulted in a total of 7,181 trainable parameters.  Overall, this neural network produced a loss of approximately 0.5627 and an accuracy of approximately 0.7266 (or 72.66%).  

![Mod20_3rdAttempt_NNStructure](https://user-images.githubusercontent.com/115128743/224512058-c33401fc-7745-42c9-b55f-6863620a8726.png)

![Mod20_3rdAttemptEvaluation](https://user-images.githubusercontent.com/115128743/224512060-cb9cbf74-e5d7-44fc-9b4c-ebbb5e936b18.png)



## Summary
Overall, we see that we were unsuccessful in generating a neural network model that would predict good candidates for donations with an accuracy of greater than 75%, despite changing the activation functions and number of total neurons.  Out of the four neural networks listed above, we see that the model with two hidden layers seemed to generate the highest accuracy, though by a very small margin.  For future attempts, it may be beneficial to try to determine which feature columns are the most influential relative to training the neural network model, and removing those columns that do not strongly affect the outcome of the neural network’s predictions.  In addition to this, we could try using a different type of model altogether, as opposed to focusing solely on neural networks.

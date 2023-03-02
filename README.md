# deep-learning-challenge

## OVERVIEW

The purpose of this analysis is to use the features in a large metadata set to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup, a fictional nonprofit foundation.

## RESULTS 

Results: Using bulleted lists and images to support your answers, address the following questions:

* Data Preprocessing

1. What variable(s) are the target(s) for your model? The target is called IS_SUCCESSFUL (was the money used effectively, in other words) and is indicated as a binary of 1 or 0.
2. What variable(s) are the features for your model? APPLICATION_TYPE and CLASSIFICATION are both features for this model. 
3. What variable(s) should be removed from the input data because they are neither targets nor features? EIN and NAME were removed from the model since they don't contribute anything to the model. I could also have removed ORGANIZATION, USE_CASE and SPECIAL_CONSIDERATIONS () since they are not likely contributing anything meaningful, either.

* Compiling, Training, and Evaluating the Model

4. How many neurons, layers, and activation functions did you select for your neural network model, and why? I initially selected 2 layers with 8 and 16 neurons respectively. In a later version (= Starter_Code-Copy1), I tried 2 layers @ 9 and 18 neurons, then 3 layers @ 11/15/22. I added a layer and incrementally increased the neurons in order to produce better accuracy, and I did manage to achieve a modest increase most likely because of the additional layer.
5. Were you able to achieve the target model performance? 

Optimization_Eval.png

6. What steps did you take in your attempts to increase model performance?

## SUMMARY
Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.
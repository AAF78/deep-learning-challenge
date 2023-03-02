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

https://github.com/AAF78/deep-learning-challenge/blob/20967a6005b44f6037c4e8a540c7fafc233b5871/Images/Optimization_Eval.png

Top performance was at 55%:74% Loss:Accuracy, meaning the loss was marginally adequate in the top-performing model, while the accuracy fell marginally short. I didn't reach the 55%:75% I aimed to achieve.

6. What steps did you take in your attempts to increase model performance? 
I did a number of steps to increase accuracy. I adjusted the architecture first, addressing the number of layers and neurons in each. I used 4 different activation functions ('relu', 'tanh', 'sigmoid' and 'softmax') to allow the model to find the best nonlinear transformation possible. I adjusted the number of epochs 5 times to find the optimal # to run through (50, then 100, then 200, then 300, and back to 200) I also included an ensemble method (AdaBoost was used) in the Starter_Code-Copy1 attempt to address weights and decay although this wasn't a satisfactory solution ultimately. I attempted to use the Adadelta and AdamW optimization in training as well; I wanted to address weight decay and both do this. However, the AdamW is experimental and when I pipinstalled the module for applying this optimization, it gave me an error that wasn't resolvable. When I attempted the Adadelta optimizer, the model immediately fit to a 0.5592 loss: 0.7433 accuracy throughout every single epoch, which clearly wasn't the expected outcome, so I discarded that optimizer and went back to the Adam optimizer instead. 

## SUMMARY
Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation:
Overall this model objectively underperformed, but increasing the training data or removing any features that may be co-linear could help. Accuracy is data-dependent, so 74% isn't necessarily a poor outcome. Time constraints definitely affected my ability to adequately "deep-dive" into the reasons and to affect a solution. Ultimately, training a neural network is iterative and takes a lot of trial-and-error to fine-tune so more work on this would likely achieve better results.
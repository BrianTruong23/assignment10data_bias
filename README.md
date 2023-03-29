# Assignment10 Data_bias

## Steps:

1. Set Up Toxic Threshold
2. Set up hypothesis
3. Set Up Example for the toxic tests.
4. Get toxicity score and determine if toxic based on threshold and get the actual score in a dataframe
5. Evaluate the fairness of the model
6. Finding and Results

## Detailed Explanation

### 1. Set up Toxic Threshold

As the average of toxicity score for non-toxic comments is around 0.11 and the average of toxicity score for toxic comments is around 0.76, I would choose the threshold of toxicity around 0.4.

### 2. Set up hypothesis

My hypothesis is that Perspective will be more likely to mark the comment with all-caps words as toxic when compared to non-cap words.

### 3. Set Up Example for the toxic tests.

I set up some examples for test cases with cap and non-cap sentences.

### 4. Get toxicity score and determine if toxic based on threshold and get the actual score in a dataframe

Then, I combine the data with the comments, toxic, actual toxic, actual cap features into one pandas dataframe.

### 5. Evaluate the fairness of the model

I evaluate the fairness of the model by using a function taught in class to determine how may cases the model got it wrong or right for both cases of all-cap or non-cap.

### 6. Finding and Results

#### Results

- Class 1 (toxic) accuracy for all_cap = 1.0
- Class 0 (non_toxic) accuracy for all_cap = 0.6666666666666666
- Class 1 (toxic) accuracy for non_cap = 1.0
- Class 0 (non_toxic) accuracy for non_cap = 1.0

#### Findings

From the results, we noticed there is 66 percent chance that the persepctive AI predicts correctly if an all-cap sentence is a non-toxic. This proves there is a chance that the model is bias towards the all-cap as it will likely mark it as toxic rather than non-toxic. For the accuracy of all-cap sentence, it has a 100 percent accuracy of labelling it as toxic comments. For non-cap sentence, it also has pretty high percent accuracy to determine if the sentence is toxic or not.

Because the test sample is very small, the results may not be reliable. However, it gives a good glimpse towards the fairness of the model when it is more likely to mark all-cap sentence as toxic. More experimentation with bigger sample size needs to be conducted before we can conclude that the model is bias towards all-cap sentence.

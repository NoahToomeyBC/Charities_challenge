# Analysis of Charities using Neural Networks

## Overview of the analysis

In this project, we looked for a way to start building a neural network that will assist the Alphabet Soup Charity foundation in detecting which charities are most likely to be legitimate and, by extension, mosty likely to be approved of for additional funding through Alphabet Soup. By utilizing tensorflow we were able to set the foundation for further study using machine learning and neural networks. While the model was unable to reach a level where we felt confident in utilizing the metrics found as a decision-making tool, this model sets the framework for further study and experimentation with neural networks. 

## Results: 

### Data Preprocessing

- What variable(s) are considered the target(s) for your model?
    - The target for this model was the column IS_SUCCESFUL as that is what we are judging the effectiveness of the model off of.

- What variable(s) are considered to be the features for your model?
    - Every column in our model would be considered a feature besides IS_SUCCESFUL, EIN, and NAME, the latter two were removed entirely.
    - APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT would all be considered potential features.

- What variable(s) are neither targets nor features, and should be removed from the input data? 
    - Both EIN and NAME were removed due to them being the name and id of the organizations which is not able to be quantified like the other features listed above.

### Compiling, Training, and Evaluating the Model

- How many neurons, layers, and activation functions did you select for your neural network model, and why?
![layer_info](https://user-images.githubusercontent.com/85508764/138615135-bdb55a33-c900-4f40-b478-b4b543a7e639.png)
    - Neurons:
        - Layer 1: 100
        - Layer 2: 50
        - Layer 3: 35
    - Layers: Three were hidden layers and then one final layer for our output.
    - Activation functions:
        - Layer 1: relu
        - Layer 2: relu
        - Layer 3: relu
        - Final layer: Sigmoid was selected due to the binary nature of the output we were looking for.

- Were you able to achieve the target model performance?
    - We were unable to reach the target model performance of .75.

- What steps did you take to try and increase model performance?
    - In order to increase the model perfromance we attempted to increase the neurons, number of layers, and removing the ORGANIZATION column.

## Summary

![results](https://user-images.githubusercontent.com/85508764/138615140-810b97c0-274c-4dd4-afe2-c7d539b82da7.png)

While neural networks are effective at getting precise outcomes, the internal workings of the algorithms are something of a mystery. We would suggest potentially using a supervised learning model so that additional information can be gleaned from the results which will help make informed decisions about whether or not to give applicants funding.

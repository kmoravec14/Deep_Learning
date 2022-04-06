1.  **Overview** of the analysis: Explain the purpose of this analysis.
    * To develop a machine learning method to predict which charity submissions were likely to be successful

2. **Results**: Using bulleted lists and images to support your answers, address the following questions.

  * Data Preprocessing
    * Target Variable: 
        * Is Successful
    * Feature Variables:
        * Application Type
        * Affiliation
        * Classification
        * Use_Case
        * Organization
        * Status
        * Income_Amt
        * Special_Considerations
        * Ask_Amt
        
    * What variable(s) are neither targets nor features, and should be removed from the input data?
        * EIN Number
        * Name
  * Compiling, Training, and Evaluating the Model
    * How many neurons, layers, and activation functions did you select for your neural network model, and why?
        * Neurons: Initial choice = 9:  Matched Number of Input Variables
        * Hidden Layers = 2:  Chosen to be approximately 25% of Neurons
        * Hidden Activation Function = Relu: Chosen based on good performance in class for classification problems
        * Output Activation Fuction = Sigmoid:  Chosen because this is a classification problem
    * Were you able to achieve the target model performance?
        * Goal of 75% accuracy of predicting target variable was not achievd
    * What steps did you take to try and increase model performance?
        * 1st Pass Accuracy - Accuracy: 0.7278134226799011
        * With Binning Ask_Amt - Accuracy: 0.7231487035751343 (Worse)
        * With 36 Neurons in each layer (was 9) - Accuracy: 0.727580189704895 (Worse than 1st pass)
        * With 3 layers (was 2) - Accuracy: 0.7245481014251709 (Worse than 1st pass)
        * With tanh activation fuction - Accuracy: 0.7264139652252197 (Worse than 1st pass)
        * With 1 hidden layer (was 2) - Accuracy: 0.7241982221603394 (Worse than 1st pass)

3. **Summary**: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.
       * I would recommend trying a randomm forest model.  Random forest models tend to predict classification problems well.  Caution not to overfit should be used.
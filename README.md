### Overview

The purpose of this project is to develop a machine learning model that predicts employee attrition (whether an employee will leave the company) and department assignment (which department an employee belongs to) based on various factors. These factors include age, travel frequency, education level, job satisfaction, marital status, and more. This project encompasses multiple stages: data preprocessing to prepare the dataset for analysis, neural network creation to build the predictive model, model training to fit the model to the data, and evaluation to assess the model's performance. By accurately predicting attrition and department assignment, companies can better understand their workforce and implement strategies to improve employee retention and satisfaction.

### Functionality

1. **Preprocessing**: 
   - **train_test_split**: Splits the data into training and testing sets to evaluate the model's performance.
   - **StandardScaler**: Standardizes features by removing the mean and scaling to unit variance.
   - **pd.get_dummies**: Converts categorical variables into a one-hot encoded format.
   - **OneHotEncoder**: Encodes categorical columns (Department and Attrition) into a format suitable for neural network training.

2. **Neural Network Creation**:
   - **Input Layer**: Accepts the preprocessed feature set.
   - **Shared Layers**: Two shared dense layers (64 and 32 neurons) with ReLU activation function, providing a common representation of the input data.
   - **Department Branch**:
     - **Hidden Layer**: A dense layer with 16 neurons and ReLU activation function.
     - **Output Layer**: A dense layer with softmax activation to predict the department.
   - **Attrition Branch**:
     - **Hidden Layer**: A dense layer with 16 neurons and ReLU activation function.
     - **Output Layer**: A dense layer with softmax activation to predict attrition status.

3. **Training and Evaluation**:
   - **model.compile**: Compiles the model with Adam optimizer and categorical cross-entropy loss for both outputs.
   - **model.fit**: Trains the model on the training data for 100 epochs.
   - **model.evaluate**: Evaluates the model's performance on the test data.
   - **Accuracy Calculation**: Calculates the accuracy for both department and attrition predictions.

### Summary

In summary, what was found was that the neural network model could predict employee attrition and department assignment with moderate accuracy. The model achieved approximately 80% accuracy in predicting attrition but was less accurate in predicting department assignment, with about 56% accuracy. These results suggest that while the model is relatively good at identifying employees at risk of leaving, it struggles more with accurately classifying the department.

**Reflection**:
The findings highlight the potential and limitations of the model. The high attrition prediction accuracy is useful for HR departments to identify and address factors leading to employee turnover. However, the lower accuracy in department prediction indicates that additional data features or alternative modeling approaches may be necessary to improve this aspect. This project demonstrates the importance of feature selection and model evaluation in developing effective predictive models for real-world applications.

**Real-World Applications**:
1. **Human Resources**: Companies can use this model to predict which employees are at risk of leaving, enabling proactive measures such as offering incentives, improving working conditions, or addressing individual concerns to improve retention rates.
2. **Workforce Planning**: This model helps in assigning employees to the most suitable departments based on their profiles, enhancing job satisfaction, productivity, and overall employee performance.

# Deep Learning Regression with Admissions Data

This model predicts the accpetance rate of graduate school based on 7 factors such as test scores, quality of statement of purpose, GPA, etc. with a dataset of 500 students.
For applicants, it can be used to identify weak areas and strategize their target selection of universities. This model can be useful for the admission committees as well to reduce bias and identify candidates efficiently.

Enjoy my first journey of making a deep learning model!

## Step 1: Explore Data
First step was to explore the data by creating separate dataframe for its features and labels. The "Chance_of_admit" at the last column is a continuous label between 0 and 1 which makes this a regression problem rather than categorical.
![image](https://github.com/user-attachments/assets/75d54262-8b2a-4a3a-a5ba-8903d63e488e)

## Step 2: Preprocess Data
Before building the model, the features and labels were split again into train set and test set to test how well it generalizes to unseen data. This is a fairly small dataset, so the test size is 20% and train size is 80%.
Linear Regression was printed to compare it with my deep learning model with R-squared (R2): 0.8188432567829629 and mean-squared (MSE): 0.003704655398788409
![image](https://github.com/user-attachments/assets/340f1507-5d9f-4eef-bd57-8b6001b08ac2)

## Step 3: First Model
The first model returned pretty bad R2 and MSE values of 0.5787923551775567 and 0.008613696321845055 indicating that the model is not learning the train set well.
![image](https://github.com/user-attachments/assets/09dfa660-c44d-4bdf-8282-e748ea99a310)

## Step 4: Random Search
Random search helped tune the parameters from the first model for quick approximation of the best parameters, suggesting batch size of 13 and epochs of 64.
![image](https://github.com/user-attachments/assets/50168e86-97cf-4c3e-a781-a1ccd782ed74)

## Step 5: Second Model
In addition to random search, we added a drop out layer to improve generalization. The R2 value returned closer to 1 with 0.811995964815107, and the MSE values returned closer to 0 with 0.0038446825928986073!!
![image](https://github.com/user-attachments/assets/8cbaa68c-0430-4b0f-a14b-4ea62f8ecb35)
![image](https://github.com/user-attachments/assets/475dd968-1a9d-41dd-aa12-d60aab85a889)

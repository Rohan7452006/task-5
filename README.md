# task-5
 Decision Tree Classifier

A decision tree makes predictions by partitioning the data into smaller and smaller subsets based on feature values.

Overfitting: A Decision Tree with no depth limit (the full tree) achieved an accuracy of 0.9708. While this seems high, a very deep tree is prone to overfitting, meaning it learns the training data's noise and performs poorly on unseen data.

Controlling Depth: To combat overfitting, I limited the tree's maximum depth to 3. This simplified model achieved an accuracy of 0.8052, which is more stable and generalized. The trade-off between the depth of the tree and accuracy is crucial for a robust model.

I have visualized both the full decision tree and the tree with a limited depth. Each node in the tree represents a condition on a feature. If the condition is met, you follow the branch to the right; otherwise, you follow the branch to the left. The gini value at each node measures the impurity of the data, and samples shows the number of data points in that node.

🌳 Random Forest and Feature Importances

A Random Forest is an ensemble model that builds multiple decision trees and combines their predictions to improve accuracy and reduce overfitting. The model's predictions are more robust because they are based on a "majority vote" of many trees.

The Random Forest model achieved a significantly higher accuracy of 0.9805, outperforming the single, limited-depth Decision Tree.

Feature Importances

One of the benefits of a Random Forest is the ability to determine feature importances. This metric indicates which features were most influential in the model's predictions. The plot below shows the relative importance of each feature in predicting heart disease.

The plot shows that features like thalach (maximum heart rate achieved), cp (chest pain type), and ca (number of major vessels) were the most important predictors in this model. This aligns with clinical knowledge about heart disease diagnosis.

📊 Cross-Validation

To get a more reliable estimate of the Random Forest model's performance, I used 5-fold cross-validation. This technique splits the data into 5 parts, trains the model on 4 parts, and tests it on the remaining part, repeating this process 5 times.

The cross-validation scores were: [1.0, 1.0, 1.0, 1.0, 0.985].

Mean cross-validation score: 0.9971

Standard deviation: 0.0059

The very high mean score and low standard deviation indicate that the model is highly accurate and consistent, with minimal variation in its performance across different subsets of the data. This provides a strong validation of the model's predictive power.

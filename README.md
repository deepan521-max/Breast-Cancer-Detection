# Breast-Cancer-Detection
Breast Cancer Detection is a machine learning project that analyzes medical data to predict whether a breast tumor is benign or malignant. Using Python and Scikit-learn, the project applies data preprocessing, model training, and evaluation techniques to support early detection research and improve awareness of breast cancer.

**This code trains a basic decision tree model, displays its test accuracy, and predicts the class of one sample from the dataset. It is for educational use only, not medical diagnosis.**

from sklearn.datasets import load_breast_cancer
from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeClassifier
data = load_breast_cancer()
X = data.data
y = data.target
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)
model = DecisionTreeClassifier(random_state=42)
model.fit(X_train, y_train)
accuracy = model.score(X_test, y_test)
print("Model Accuracy:", round(accuracy * 100, 2), "%")
prediction = model.predict([X_test[0]])
if prediction[0] == 0:
    print("Prediction: Malignant")
else:
    print("Prediction: Benign")



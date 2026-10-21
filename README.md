# Breast-Cancer-Detection
Breast Cancer Detection is a machine learning project that analyzes medical data to predict whether a breast tumor is benign or malignant. Using Python and Scikit-learn, the project applies data preprocessing, model training, and evaluation techniques to support early detection research and improve awareness of breast cancer.

**This code trains a basic decision tree model, displays its test accuracy, and predicts the class of one sample from the dataset. It is for educational use only, not medical diagnosis.**

#include <stdio.h>

int main(void) {
    float radius;
    printf("=== Breast Cancer Detection ===\n");
    printf("Enter tumor radius measurement: ");
    if (scanf("%f", &radius) != 1) {
        printf("Error: Invalid input. Enter a number.\n");
        return 1;
    }
    if (radius <= 0) {
        printf("Error: Radius must be greater than zero.\n");
        return 1;
    }
    printf("Tumor radius: %.2f\n", radius);
    printf("Measurement recorded successfully.\n");
    printf("Radius alone cannot determine whether a tumor is benign or malignant.\n");
    return 0;
}


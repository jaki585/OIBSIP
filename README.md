# 🌸 Iris Flower Classification using Machine Learning

This project focuses on classifying iris flowers into **Setosa**, **Versicolor**, and **Virginica** using machine learning algorithms.
It includes **data visualization**, **model building**, **evaluation**, and **comparison of ML models** such as **KNN** and **Decision Tree**.

---

## 📌 Project Overview

The Iris dataset is a classic dataset in machine learning containing 150 samples of iris flowers, categorized by species.
This project aims to:

* Visualize the dataset
* Train ML models
* Evaluate performance
* Compare classification results

---

## 🗂 Dataset Used

The dataset contains the following features:

* **SepalLengthCm**
* **SepalWidthCm**
* **PetalLengthCm**
* **PetalWidthCm**
* **Species**

Species include:

* *Iris-setosa*
* *Iris-versicolor*
* *Iris-virginica*

---

## 🛠️ Technologies & Libraries

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **Scikit-Learn**

  * KNN Classifier
  * Decision Tree Classifier
  * Train-Test Split
  * Label Encoding

---

## 📊 Data Visualization

A scatter plot is used to visualize the relationship between **Petal Length** and **Petal Width**, colored by species.

```python
plt.figure(figsize=(8, 6))
sns.scatterplot(
    x='PetalLengthCm', 
    y='PetalWidthCm', 
    hue='Species', 
    data=df, 
    palette='viridis',
    s=70
)
plt.title('Iris Species Classification by Petal Dimensions')
plt.xlabel('Petal Length (cm)')
plt.ylabel('Petal Width (cm)')
plt.legend(title='Species')
plt.grid(True, linestyle='--', alpha=0.6)
plt.show()
```

This visualization helps understand how the species are naturally separated based on flower measurements.

---

## 🤖 Machine Learning Models

### ✅ 1. K-Nearest Neighbors (KNN)

* Simple and effective classification algorithm
* Performs well on this dataset
* Often achieves accuracy above **95%**

### ✅ 2. Decision Tree Classifier

A second model was tested to compare performance.

```python
dt_model = DecisionTreeClassifier(random_state=42)
dt_model.fit(X_train, y_train)
dt_pred = dt_model.predict(X_test)

print("\n--- Decision Tree Classification Report ---")
print(classification_report(y_test, dt_pred, target_names=le.classes_))
```

The evaluation includes:

* Precision
* Recall
* F1-Score
* Accuracy

---

## 📈 Model Evaluation Metrics

Both models are evaluated using:

* **Confusion Matrix**
* **Classification Report**
* **Accuracy Score**

This helps compare which algorithm performs best.

---

## 🚀 How to Run This Project

1. Clone the repository:

```
git clone https://github.com/your-username/your-repository.git
```

2. Install dependencies:

```
pip install -r requirements.txt
```

3. Run the notebook or script:

```
python iris_classification.py
```

Or open in **Google Colab**.

---

## 📌 Future Improvements

* Add SVM, Random Forest, and Logistic Regression
* Build a Streamlit web app for live predictions
* Add more visualizations (pairplot, heatmap)
* Save models using pickle

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

---

## ⭐ Support This Project

If you found this project helpful, please **star ⭐ the repository**.

---

## 📝 License

This project is free and open-source.

---


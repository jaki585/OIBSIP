import matplotlib.pyplot as plt
import seaborn as sns

# Make sure you installed seaborn and matplotlib: pip install seaborn matplotlib

# Create a scatter plot of Petal Length vs. Petal Width, colored by Species
plt.figure(figsize=(8, 6))
sns.scatterplot(
    x='PetalLengthCm', 
    y='PetalWidthCm', 
    hue='Species', 
    data=df, 
    palette='viridis',
    s=70 # size of dots
)
plt.title('Iris Species Classification by Petal Dimensions')
plt.xlabel('Petal Length (cm)')
plt.ylabel('Petal Width (cm)')
plt.legend(title='Species')
plt.grid(True, linestyle='--', alpha=0.6)
plt.show() 
# ```

### 2. Trying Another Model

The KNN model worked well, but data scientists often test multiple models. A **Decision Tree Classifier** is another simple and interpretable model.

```python
from sklearn.tree import DecisionTreeClassifier

# Initialize and train the Decision Tree Model
dt_model = DecisionTreeClassifier(random_state=42)
dt_model.fit(X_train, y_train)

# Make predictions
dt_pred = dt_model.predict(X_test)

# Evaluate
print("\n--- Decision Tree Classification Report ---")
print(classification_report(y_test, dt_pred, target_names=le.classes_))

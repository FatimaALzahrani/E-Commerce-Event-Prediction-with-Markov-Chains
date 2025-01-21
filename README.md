![header](https://capsule-render.vercel.app/api?type=rect&height=300&color=gradient&text=E-Commerce%20Event%20Prediction%20with%20Markov%20Chains&customColorList=25&fontSize=34)

This repository contains a project focused on predicting user behavior in an e-commerce setting using Markov Chains. The dataset consists of user interactions with products, and the goal is to predict the sequence of events (view, cart addition, purchase) based on prior user actions. The project includes data cleaning, visualization, model building, and evaluation.

---

## **Table of Contents** 📚

- [Project Overview](#project-overview)
- [Installation](#installation)
- [Dataset](#dataset)
- [Usage](#usage)
  - [Data Cleaning](#data-cleaning)
  - [Data Visualization](#data-visualization)
  - [Markov Chain Prediction](#markov-chain-prediction)
  - [Model Evaluation](#model-evaluation)
- [Results](#results)
- [License](#license)
- [Acknowledgements](#acknowledgements)

---

## **Project Overview** 📖

In this project, we analyze an e-commerce dataset to explore user interaction behaviors using Markov Chains. The dataset tracks user actions such as viewing, adding products to the cart, and making purchases. By calculating transition matrices, we predict the likelihood of users moving from one event type to another. We also visualize the data to gain insights into user behavior patterns and evaluate the prediction model's performance.

---

## **Installation** ⚙️

To use this repository, clone it to your local machine and install the required Python libraries.

1. Clone the repository:
    ```bash
    git clone https://github.com/FatimaALzahrani/E-Commerce-Event-Prediction-with-Markov-Chains.git
    ```

2. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

The required libraries include:
- `pandas`
- `numpy`
- `seaborn`
- `matplotlib`
- `scikit-learn`
- `google.colab`

---

## **Dataset** 📑

The dataset used in this project is stored as a CSV file and contains information about user actions on an e-commerce platform. The key columns include:
- `event_type`: The type of user action (view, cart, purchase).
- `user_id`: Unique identifier for the user.
- `product_id`: Unique identifier for the product.
- `price`: Price of the product involved in the event.
- `category_code`: The category of the product.
- `brand`: The brand of the product.

Ensure that the dataset is placed in the correct directory, or update the file path in the code.

---

## **Usage** 🎬

### **Data Cleaning** 🧹

To clean the dataset, use the following function:

```python
data = load_and_clean_data(file_path)
```

This function removes rows with missing values in critical columns (`event_type`, `user_id`, `product_id`, `price`), fills missing values in non-critical columns, and filters out invalid rows (e.g., with zero or negative prices).


---

### Data Visualization 📊

Several visualizations are included to explore the dataset:

- **Price Distribution**: Histogram to visualize the distribution of product prices.
  ![image](https://github.com/user-attachments/assets/783e6cec-5d7e-4273-b212-6475e47dccbd)

- **Event Type Breakdown**: Count plot to show the frequency of each event type.
  ![image](https://github.com/user-attachments/assets/6496e62e-07e6-48b9-9e1c-79c4d48a210e)

- **Event Type vs. Product Categories Heatmap**: Heatmap to visualize the relationship between product categories and event types.
![image](https://github.com/user-attachments/assets/63c5d53b-74b1-4ac0-aa5b-974ce1742ea0)

---

### Markov Chain Prediction 🤖

The Markov Chain model predicts the future sequence of user actions. Use the function `markov_chain_prediction(matrix, states, start_state, days)` to simulate predictions over a specified number of days.

```python
predicted_states = markov_chain_prediction(transition_matrix, states, start_state, days=30)
```
---

### Model Evaluation 🧮

After generating predictions, the model’s performance is evaluated using:

- **Accuracy**
- **Precision**
- **Recall**
- **Confusion Matrix**
- **Classification Report**

![image](https://github.com/user-attachments/assets/2b804e0c-4582-485a-b94e-f845f3eb74e5)

---

### Results 📈

The results of the model, including the transition matrix, predicted states, and cleaned dataset, can be found in the following files:

- `transition_matrix.csv`: The transition matrix of state probabilities.
- `predictions.csv`: The predicted and true states.
- `cleaned_dataset.csv`: The cleaned dataset after preprocessing.
<?--

### Acknowledgements 🙏

- **Markov Chains**: For providing a foundation for probabilistic event prediction.
- **Seaborn and Matplotlib**: For visualization libraries that helped in generating insightful plots.
- **Scikit-learn**: For evaluation metrics that helped in assessing model performance.
-->

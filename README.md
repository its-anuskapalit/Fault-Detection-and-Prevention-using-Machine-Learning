# Fault-Detection-and-Prevention-using-Machine-Learning
# Fault Detection and Prevention using Machine Learning

## 📌 Project Overview
This project aims to **detect irregularities in energy consumption patterns** using machine learning techniques. The system utilizes an **autoencoder-based anomaly detection model** to analyze temperature variations and identify faults or anomalies in energy usage.

## 🚀 Features
- **Anomaly Detection**: Identifies irregularities based on temperature inputs.
- **Machine Learning Model**: Uses an autoencoder neural network for unsupervised anomaly detection.
- **Web Interface**: Interactive UI built with Streamlit for easy input and visualization.
- **Threshold-based Evaluation**: Computes reconstruction errors to classify data as normal or anomalous.


## 🔧 Installation
### Prerequisites
Ensure you have Python installed. You can set up the environment using the following steps:

```sh
# Clone the repository
git clone https://github.com/yourusername/fault-detection.git
cd fault-detection



### 2️⃣ Using the Model in a Script
```python
from model import predict_anomaly

# Example input
min_temp, center_temp, max_temp = 30, 60, 90
result = predict_anomaly(min_temp, center_temp, max_temp)

print(f"Anomaly detection result: {'ANOMALY' if result['is_anomaly'] else 'NORMAL'}")
```

## 📊 Model Details
- **Model Type**: Autoencoder
- **Input Features**: min_temp, center_temp, max_temp
- **Loss Function**: Mean Squared Error (MSE)
- **Evaluation Metric**: Reconstruction error

## ⚠️ Troubleshooting
### ❌ ValueError: Expected shape=(None, 4), found shape=(1, 3)
- Ensure that the model was trained on **only three features** (min_temp, center_temp, max_temp).
- If the model expects four features, add a placeholder feature (e.g., `0`).

```python
input_data = np.array([[0, min_temp, center_temp, max_temp]])
```

## 📜 License
This project is licensed under the MIT License. See `LICENSE` for details.

## 🤝 Contributing
Feel free to fork, open issues, or submit pull requests to improve the project.

## 📩 Contact
For questions or collaboration, reach out at [your-email@example.com].


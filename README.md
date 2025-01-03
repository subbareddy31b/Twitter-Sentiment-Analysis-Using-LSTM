# ✈️ Twitter Sentiment Analysis Using LSTM 🌟

## 🚀 Overview
- Analyze airline-related tweets 🐦 to determine customer sentiments 😊 😡 😐 using **LSTM (Long Short-Term Memory)** models. This project leverages the **Twitter US Airline Sentiment** dataset to classify tweets into **positive**, **negative**, and **neutral** sentiments.  
---

## 📄 Dataset  
📂 The dataset used is the [**Twitter US Airline Sentiment**](https://www.kaggle.com/datasets/crowdflower/twitter-airline-sentiment). It contains:  
- 📝 **14,640 entries** representing customer reviews.  
- 🧮 **15 features**, including tweet metadata, sentiment labels, and reasons for sentiments.  

### 📊 Sentiment Distribution:  
- 😊 **Positive**: 2,363  
- 😐 **Neutral**: 3,099  
- 😡 **Negative**: 9,178  
---

## 🛠️ LSTM Architectures  

### 🏗️ **Base LSTM Model:**  
1. **📚 Embedding Layer**: Maps vocabulary into 32-dimensional space.  
2. **⚙️ Conv1D Layer**: Applies 32 filters with ReLU activation and MaxPooling1D.  
3. **🔄 Bidirectional LSTM Layer**: 64 units for capturing forward and backward dependencies.  
4. **🚧 Dropout Layer**: Dropout rate of 0.5 to reduce overfitting.  
5. **🎯 Output Layer**: Dense layer with 3 units using the **softmax** activation function for classification.  

#### 🧪 **Performance:**  
- 🟢 **Initial Learning**: Rapid learning with increasing accuracy and decreasing loss.  
- 🔴 **Overfitting**: Validation loss increases after a few epochs.
- 🎯 **Accuracy**: 71%
---

### 🏗️ **Improved LSTM Model:**  
1. **📚 Embedding Layer**: Similar to the base model.  
2. **🔄 First Bidirectional LSTM Layer**: 64 units to capture dependencies in both directions.  
3. **🚧 Dropout Layer**: Prevents overfitting with a dropout rate of 0.5.  
4. **🔄 Second Bidirectional LSTM Layer**: Another 64-unit layer for deeper learning.  
5. **🎯 Output Layer**: Dense layer with 3 units and **sigmoid** activation for classification.  

#### 🧪 **Performance:**  
- 🟢 **Consistent Learning**: Gradual improvement in validation accuracy.  
- 🟡 **Better Generalization**: Reduced overfitting compared to the base model.
- 🎯 **Accuracy**: 76%
---

## 📊 Key Results  
- 🟢 **Base Model**: Rapid learning but prone to overfitting.  
- 🟡 **Improved Model**: Balanced training and validation with better performance.  
---

## 📈 Visualizations  

### 🧩 Sentiment Distribution 📊  
A breakdown of positive, neutral, and negative sentiments in the dataset.  
![output](https://github.com/user-attachments/assets/aa60e4f5-abcb-461d-b69d-4fb64b654dae)

### 📊 Prediction Accuracy and Loss 📉  
Plots showcasing model training and validation performance over epochs.  
![output](https://github.com/user-attachments/assets/130bd463-d761-4375-a46d-fa74be6eea67)


### 🔥 Confusion Matrix 🔢  
Illustrates how well the models classify the three sentiment categories.  
![output](https://github.com/user-attachments/assets/5551d605-26de-407b-ae50-8f16066ee94b)

---

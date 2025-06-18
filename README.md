# Maternal_Health_Summative

# Optimization Techniques in Machine Learning for Maternal Health Risk Prediction

## 📌 Project Overview
This project explores optimization techniques for machine learning models to predict maternal health risk levels (Low/Medium/High) using health metrics from Rwandan women. The implementation compares:
- Neural networks with different regularization/optimization configurations
- A baseline Random Forest model

## 🎯 Objectives
1. Implement and compare 4 neural network architectures with different optimization techniques
2. Evaluate model performance using F1-score, precision, recall, and confusion matrices
3. Identify the best-performing model for deployment

## 📂 Dataset
**Maternal Health Risk Data Set** containing:
- **Features**: Blood pressure, heart rate, age, temperature, etc.
- **Target**: Risk level (0=Low, 1=Medium, 2=High)
- **Samples**: 1,034 observations

## 🛠️ Implementation

### Model Architectures
| Model | Architecture | Optimization | Regularization | Dropout | Learning Rate |
|-------|--------------|--------------|----------------|---------|---------------|
| Model 1 | 64-32-3 | Adam | None | 0% | 0.001 |
| Model 2 | 64-32-3 | Adam | L2 | 30% | 0.0005 |
| Model 3 | 64-32-3 | RMSprop | L1 | 20% | 0.0002 |
| Model 4 | 64-32-3 | Adam | L2 | 40% | 0.0003 |

### Key Techniques Compared:
- **Regularization**: L1 vs L2
- **Optimizers**: Adam vs RMSprop
- **Dropout**: 0-40%
- **Learning Rates**: 0.0002-0.001

## 📊 Results

### Performance Comparison
| Model | Accuracy | F1-Score | Precision | Recall | Loss |
|-------|----------|----------|-----------|--------|------|
| RandomForest | 0.8374 | 0.8384 | 0.8417 | 0.8374 | 0.4179 |
| Model 4 | 0.6897 | 0.6643 | 0.7100 | 0.6897 | 0.7436 |
| Model 1 | 0.6798 | 0.6743 | 0.6823 | 0.6798 | 0.6748 |
| Model 2 | 0.6650 | 0.6501 | 0.6678 | 0.6650 | 0.7292 |
| Model 3 | 0.6355 | 0.5928 | 0.6665 | 0.6355 | 0.8597 |

### Best Model
**Random Forest Classifier** outperformed neural networks with:
- **Accuracy**: 83.74%
- **F1-Score**: 83.84%
- **Precision**: 84.17%

![Confusion Matrix](images/confusion_matrix.png)
*Confusion matrix for the best model*

## 💡 Key Findings
1. The Random Forest model achieved superior performance compared to neural networks
2. Among neural networks:
   - L2 regularization (Model 4) performed best
   - Lower learning rates (0.0002-0.0005) showed better stability
   - Dropout (30-40%) helped prevent overfitting
3. Model 4 (L2 + 40% dropout) was the best neural network with 68.97% accuracy

## 🚀 How to Use
1. Install requirements:
   ```bash
   pip install -r requirements.txt

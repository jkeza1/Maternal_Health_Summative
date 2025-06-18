# Maternal_Health_Summative
 **Keza Joan**
**BSE Year 3, African Leadership University**
# Optimization Techniques in Machine Learning for Maternal Health Risk Prediction

## 🌍 Motivation & Background
Unplanned pregnancies among single mothers in Rwanda contribute to:
- Cycles of poverty and school dropouts
- Poor maternal/neonatal health outcomes
- Strain on community health resources

While platforms like RapidSMS and Babyl Rwanda provide health tracking, they lack predictive capabilities for personalized interventions in low-resource settings.

## 📌 Problem Statement
This project predicts maternal health risk levels (Low/Medium/High) using health metrics from Rwandan women. We compare neural networks with different optimization techniques against classical ML algorithms to identify the most effective approach for community health applications.

## Project Overview
This project explores optimization techniques for machine learning models to predict maternal health risk levels (Low/Medium/High) using health metrics from Rwandan women. The implementation compares:
- Neural networks with different regularization/optimization configurations
- A baseline Random Forest model
- 
**Our Solution:**
Predict pregnancy risk using accessible community-collected data to enable:
- Early interventions through Rwanda's SMEEF platform
- Targeted support for high-risk women
- Resource optimization for community health programs
## 🎯 Objectives
1. Implement and compare 4 neural network architectures with different optimization techniques
2. Evaluate model performance using F1-score, precision, recall, and confusion matrices
3. Identify the best-performing model for deployment

## 📂 Dataset
**Maternal Health Risk Data Set** containing:
- **Features**: Blood pressure, heart rate, age, temperature, etc.
- **Target**: Risk level (0=Low, 1=Medium, 2=High)
- **Samples**: 1,034 observations

## 🏗️ Implementation

### Model Architectures

#### Neural Networks
| Instance | Optimizer | Regularizer | Epochs | Early Stopping | Layers | Learning Rate | Dropout | Accuracy | F1-Score | Precision | Recall |
|----------|-----------|-------------|--------|----------------|--------|---------------|---------|----------|----------|-----------|--------|
| 1 (Baseline) | Adam | None | 20 | No | 3 | 0.001 | 0% | 0.6798 | 0.6743 | 0.6823 | 0.6798 |
| 2 | Adam | L2 | 30 | Yes | 3 | 0.0005 | 30% | 0.6650 | 0.6501 | 0.6678 | 0.6650 |
| 3 | RMSprop | L1 | 25 | No | 3 | 0.0002 | 20% | 0.6355 | 0.5928 | 0.6665 | 0.6355 |
| 4 | Adam | L2 | 35 | Yes | 3 | 0.0003 | 40% | 0.6897 | 0.6643 | 0.7100 | 0.6897 |

#### Classical ML (Random Forest)
| Model | n_estimators | max_depth | min_samples_split | Accuracy | F1-Score | 
|-------|--------------|-----------|-------------------|----------|----------|
| Optimized RF | 200 | 20 | 2 | 0.8374 | 0.8384 |

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

### Best Performing Models
1. **Random Forest Classifier** (Best Overall)
   - Accuracy: 83.74%
   - Key Hyperparameters: 
     - `n_estimators=200`
     - `max_depth=20`
     - `min_samples_split=2`

2. **Neural Network (Instance 4)** (Best NN)
   - Accuracy: 68.97%
   - Configuration:
     - L2 Regularization
     - 40% Dropout
     - Learning Rate: 0.0003

## 💡 Key Findings
1. The Random Forest model achieved superior performance compared to neural networks
2. Among neural networks:
   - L2 regularization (Model 4) performed best
   - L2 regularization worked better than L1
   - Lower learning rates (0.0002-0.0005) showed better stability
   - Dropout (30-40%) helped prevent overfitting
3. Model 4 (L2 + 40% dropout) was the best neural network with 68.97% accuracy


   ### Video
## [Watch the video ](https://youtu.be/LBi41Ysy4Bg)



 

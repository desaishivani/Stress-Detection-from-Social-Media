# **Stress Detection from Social Media**

## 📌 **Project Overview**  

The rapid rise of social media has led to growing concerns about its impact on mental health. Stress detection from textual content shared on platforms like Reddit and Twitter offers valuable insights into understanding mental well-being and creating actionable interventions. This project focuses on detecting stress from social media texts using machine learning (ML) models and state-of-the-art natural language processing (NLP) techniques.

**Key Objectives**:  
1. Analyze stress-related textual data sourced from Reddit and Twitter.  
2. Identify frequent indicators of stressful and non-stressful content.  
3. Train ML models to accurately classify social media content as stress-positive or stress-negative.  
4. Benchmark results with models like Decision Trees, SVM, Logistic Regression, and XGBoost.  


## 🛠️ **Methodology**

### **Dataset**  
- **Source**: Kaggle - "Stress Detection from Social Media Articles" dataset.  
- **Data Details**:  
  - 5,174 records, including texts from Reddit and Twitter.  
  - Binary labels:  
    - `0`: Stress Negative  
    - `1`: Stress Positive  
  - Features:  
    - **Text**: Social media content.  
    - **Label**: Stress indicator.  

### **Data Preparation**  
1. **Cleaning**:  
   - Removed missing entries.  
   - Converted text to lowercase.  
   - Removed stop words and performed stemming.  
2. **Balancing**:  
   - Addressed class imbalance using **SMOTE (Synthetic Minority Oversampling Technique)**, achieving a balanced dataset (50/50 split).  
3. **Feature Engineering**:  
   - Extracted features using the **Bag-of-Words** and **TF-IDF** methods.  
   - Leveraged **BERT embeddings** for deep contextual understanding of the text.  

### **Models Implemented**  
1. **Decision Tree**  
2. **Logistic Regression**  
3. **Support Vector Machine (SVM)**  
4. **XGBoost**  
5. **Topic Modeling with SVD**  

### **Evaluation Metrics**  
- **Accuracy**  
- **Precision**  
- **Recall**  
- **F1-score**  
- **Confusion Matrix**  
- **ROC Curve**  


## 📈 **Results**

### **ML Model Performance**  
| **Model**           | **Accuracy** | **Precision (Neg/Pos)** | **Recall (Neg/Pos)** | **F1 (Neg/Pos)** |
|----------------------|--------------|--------------------------|-----------------------|-------------------|
| **Decision Tree**    | 80.8%        | 0.78 / 0.84             | 0.85 / 0.76          | 0.82 / 0.80       |
| **Logistic Regression** | 68.9%      | 0.66 / 0.73             | 0.78 / 0.59          | 0.72 / 0.66       |
| **SVM**              | 73.1%        | 0.68 / 0.82             | 0.87 / 0.59          | 0.76 / 0.69       |
| **XGBoost**          | 94.6%        | 0.91 / 0.97             | 0.97 / 0.92          | 0.94 / 0.94       |

### **Highlights**  
- **XGBoost with BERT embeddings** achieved the best accuracy (94.6%), outperforming other models in predicting stress-related content.  
- **SVM** demonstrated strong recall for negative labels, effectively identifying stress-negative posts.  
- **Topic Modeling (SVD)** revealed key themes in stress-related content, aiding interpretability and analysis.  


## 💡 **Key Insights**  
1. **XGBoost** with BERT embeddings excels at understanding nuanced linguistic features, making it the most effective model for this classification task.  
2. Balancing the dataset using **SMOTE** significantly improved model performance on the minority class (stress-negative).  
3. Traditional models like **Logistic Regression** and **Decision Tree** perform reasonably well but are outpaced by more sophisticated techniques like **XGBoost**.  


## 🔮 **Future Work**  
1. **Feature Engineering**: Explore advanced NLP techniques like transformer-based models (GPT, RoBERTa).  
2. **Larger Datasets**: Incorporate additional data sources to improve generalizability.  
3. **Real-Time Implementation**: Deploy models for live stress detection on social media platforms.  
4. **Emotion Analysis**: Extend analysis to multi-class emotion detection (e.g., anxiety, anger, joy).  

## 🤝 **Team Contributions**  
- **Shivani Desai**: Data preprocessing, Decision Tree modeling, and Results Analysis.  
- **Anders Pierson**: XGBoost modeling and hyperparameter optimization.  
- **Wesley Barnes**: Logistic Regression and SVM implementation.  
- **Megan White**: Data balancing (SMOTE) and evaluation metrics.  
- **Sundari Kala**: Topic Modeling (SVD) and visualization.  

## 📚 **References**  
1. Kaggle Dataset: ["Stress Detection from Social Media Articles"]
2. Research Paper: "Stress Detection from Social Media Articles: New Dataset Benchmark and Analytical Study."  

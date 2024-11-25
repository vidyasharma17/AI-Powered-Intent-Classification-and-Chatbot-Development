
# **AI-Powered Intent Classification and Chatbot Development**

## **Project Overview**
This project focuses on training and evaluating machine learning models for intent classification and integrating the trained models into a chatbot. It compares the performance of two approaches:
- A traditional Naive Bayes model.
- A transformer-based BERT model.

The chatbot is designed to recognize user intents and provide meaningful responses using the best-performing model. This project demonstrates the end-to-end pipeline of training, evaluation, comparison, and deployment.

---

## **Key Features**
- **Naive Bayes Model**:
  - Uses TF-IDF vectorization for feature extraction.
  - Provides a lightweight solution for intent classification.
- **BERT Model**:
  - Fine-tuned transformer model for enhanced contextual understanding.
  - Superior performance in intent classification tasks.
- **Chatbot Integration**:
  - Chatbot uses the trained BERT model to predict intents.
  - Flask-based REST API for easy interaction.

---

## **Evaluation Results**
| **Model**       | **Accuracy** | **Precision** | **Recall** | **F1-Score** |
|------------------|--------------|---------------|------------|--------------|
| Naive Bayes      | 79%          | 78%           | 79%        | 78%          |
| BERT             | 89%          | 88%           | 89%        | 88%          |

### **Observations**:
- **Naive Bayes**: Lightweight, suitable for resource-constrained environments.
- **BERT**: Superior accuracy and contextual understanding, recommended for production use.

---

## **Recommendations**
- Use BERT for production applications requiring high accuracy and contextual understanding.
- Naive Bayes is suitable for lightweight tasks or resource-limited scenarios.
- Enhance the chatbot by adding more intents and responses for improved usability.

---

## **Future Enhancements**
1. Deploy the chatbot using a production-grade server like Gunicorn or AWS Lambda.
2. Extend functionality with features like multi-language support.
3. Add advanced visualizations for model performance comparisons.





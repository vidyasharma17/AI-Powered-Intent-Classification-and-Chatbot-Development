
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

## **Project Structure**

```plaintext
.
├── data.csv               # Input dataset for training and testing
├── models/                # Saved models (Naive Bayes and BERT)
├── fintech_bert_model/    # Fine-tuned BERT model directory
├── app.py                 # Flask-based chatbot application
├── README.md              # Project documentation
└── notebooks/
    ├── model_training.ipynb  # Notebook for training models
    └── evaluation.ipynb      # Notebook for evaluation and comparison
```

---

## **Setup Instructions**

### **1. Clone the Repository**
```bash
git clone <repository_url>
cd <repository_directory>
```

### **2. Install Dependencies**
Ensure you have Python 3.7+ installed. Then, run:
```bash
pip install -r requirements.txt
```

### **3. Dataset**
Replace `data.csv` with your dataset file in the root directory. Ensure the dataset has:
- A `text` column for input text.
- A `label` column for the corresponding intents.

### **4. Train the Models**
Open the `notebooks/model_training.ipynb` file in Jupyter Notebook or a similar tool, and follow the steps to train both the Naive Bayes and BERT models.

### **5. Run the Chatbot**
After training, deploy the chatbot with Flask:
```bash
python app.py
```
Access the chatbot API at: `http://127.0.0.1:5000/chat`.

---

## **Endpoints**

### **POST /chat**
Predicts the intent of the user input and returns a response.

#### **Request**:
```json
{
    "text": "How do I activate my card?"
}
```

#### **Response**:
```json
{
    "response": "To activate your card, go to the app's settings and follow the activation instructions."
}
```

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





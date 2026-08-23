# 🎬 IMDb Sentiment Analysis Using Machine Learning & Deep Learning

A Natural Language Processing (NLP) project for classifying IMDb movie reviews into **Positive** and **Negative** sentiments using both traditional Machine Learning and Deep Learning approaches.

The project implements and compares **Logistic Regression, Linear Support Vector Machine (SVM), and Bidirectional Long Short-Term Memory (Bi-LSTM)** models through a complete text classification pipeline.

---

## 📌 Project Overview

The goal of this project is to analyze movie reviews and automatically determine their sentiment.

Three different approaches are explored:

* **Logistic Regression**
* **Linear Support Vector Machine (SVM)**
* **Bidirectional LSTM (Bi-LSTM)**

The project covers the complete NLP workflow, from text preprocessing and feature extraction to model training, evaluation, and comparison.

---

## 🎯 Objectives

* Perform binary sentiment classification on IMDb movie reviews.
* Clean and preprocess textual data.
* Apply traditional Machine Learning techniques to text classification.
* Build a Deep Learning model using Bidirectional LSTM.
* Compare different approaches using standard evaluation metrics.
* Analyze model performance using classification reports and confusion matrices.

---

## ✨ Features

* Text Cleaning and Preprocessing
* Stopword Removal
* Tokenization
* TF-IDF Feature Extraction
* Logistic Regression Classification
* Linear SVM Classification
* Bidirectional LSTM Network
* Model Performance Comparison
* Confusion Matrix Visualization
* Classification Reports
* Accuracy, Precision, Recall, and F1-Score Evaluation

---

## 📊 Dataset

**Dataset:** IMDb Movie Reviews Dataset

The dataset contains **50,000 movie reviews** with binary sentiment labels.

* **Total Reviews:** 50,000
* **Positive Reviews:** 25,000
* **Negative Reviews:** 25,000
* **Task:** Binary Sentiment Classification

### Dataset Source

[Kaggle — IMDb Dataset of 50K Movie Reviews](https://www.kaggle.com/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews)

---

## 🛠️ Tech Stack

### Programming Language

* Python

### Machine Learning

* Scikit-learn
* Logistic Regression
* Linear Support Vector Machine (SVM)

### Deep Learning

* TensorFlow
* Keras
* Bidirectional LSTM

### Natural Language Processing

* NLTK
* TF-IDF Vectorizer
* Tokenizer
* Sequence Padding

### Data Processing & Visualization

* NumPy
* Pandas
* Matplotlib
* Seaborn

---

## 🔄 Project Workflow

```text
IMDb Movie Reviews
        ↓
Data Cleaning
        ↓
Text Preprocessing
        ↓
Train-Test Split
        ↓
   ┌───────────────┐
   ↓               ↓
TF-IDF           Tokenization
   ↓               ↓
Logistic          Padding
Regression          ↓
   ↓            Bi-LSTM
Linear SVM           ↓
   ↓               ↓
   └───────┬───────┘
           ↓
   Performance Evaluation
           ↓
 Sentiment Classification
```

---

## 🧠 Machine Learning Approach

### 1. Logistic Regression

TF-IDF features are used to convert movie reviews into numerical feature vectors, which are then classified using Logistic Regression.

### 2. Linear SVM

A Linear Support Vector Machine is trained using TF-IDF features to classify reviews into positive and negative sentiment classes.

### 3. Bidirectional LSTM

A Bidirectional LSTM model processes the sequence of words in both forward and backward directions, allowing the model to capture contextual information from the review text.

---

## 📈 Evaluation Metrics

The models are evaluated using:

* **Accuracy**
* **Precision**
* **Recall**
* **F1-Score**
* **Classification Report**
* **Confusion Matrix**

These metrics provide a broader evaluation of classification performance beyond accuracy alone.

---

## 📊 Results

The project compares the performance of:

| Model               | Approach                     |
| ------------------- | ---------------------------- |
| Logistic Regression | Traditional Machine Learning |
| Linear SVM          | Traditional Machine Learning |
| Bidirectional LSTM  | Deep Learning                |

The detailed performance results, classification reports, confusion matrices, and visualizations are available in the project notebook.

---

## 📁 Project Structure

```text
imdb-sentiment-analysis/
│
├── Sentiment_Analysis_ML_DL.ipynb
├── requirements.txt
├── README.md
├── ML_Pipeline_Diagram.png
├── Bidirectional_LSTM_Architecture.png
└── screenshots/
```

---

## ⚙️ Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/milan05243/ai-ml-projects-portfolio.git
```

### 2. Navigate to the Project

```bash
cd ai-ml-projects-portfolio/imdb-sentiment-analysis
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open:

```text
Task_2_Sentiment_Analysis_ML_DL.ipynb
```

Run the notebook cells sequentially to reproduce the analysis and model training.

---

## 📐 Architecture Diagrams

The repository includes visual documentation of the project:

* **ML Pipeline Diagram**
* **Bidirectional LSTM Architecture Diagram**

These diagrams illustrate the processing pipeline and the architecture used for the deep learning model.

---

## 💡 Key Learning Outcomes

This project provided practical experience with:

* Natural Language Processing
* Text preprocessing
* TF-IDF feature extraction
* Traditional Machine Learning for text classification
* Support Vector Machines
* Logistic Regression
* Sequence processing
* Bidirectional LSTM networks
* Model evaluation
* Confusion matrix analysis
* Comparing Machine Learning and Deep Learning approaches

---

## 🔮 Future Improvements

Potential improvements for future versions include:

1. Experimenting with transformer-based models such as BERT.
2. Hyperparameter optimization for the Machine Learning models.
3. Using word embeddings such as Word2Vec or GloVe.
4. Deploying the sentiment classifier as a web application.
5. Adding an interactive interface for entering custom movie reviews.
6. Comparing additional deep learning architectures.

---

## 📄 License

This project is available under the MIT License.

---

## 👨‍💻 Author

**Milan Choudhary**

Computer Science & Engineering — Artificial Intelligence

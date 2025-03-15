# Distinguishing Mental Health Categories on Reddit Using NLP

## 📌 Project Overview
This project applies Natural Language Processing (NLP) to classify Reddit posts into different mental health categories, such as **anxiety, depression, and general well-being**. By analyzing linguistic patterns, the goal is to enhance early detection of mental health concerns and contribute to research in this field.

## 🚀 Problem Statement
With the increasing discussions on mental health platforms like Reddit, it becomes essential to systematically analyze and categorize these conversations. The challenges include:

- **Overlapping linguistic features** between different mental health conditions.
- **Noisy and unstructured data** from general discussions.
- **Imbalanced data distribution**, where certain categories are underrepresented.

This project tackles these issues using an advanced **NLP-based classification pipeline**.

---

## 🛠️ Approach
The project follows a structured NLP pipeline consisting of:

### 1️⃣ **Data Collection**
- Reddit’s **PRAW API** was used to collect posts from mental health-related subreddits:
  - `r/depression`
  - `r/Anxiety`
  - `r/SuicideWatch`
  - General subreddit (`r/CasualConversation`) as a control group.

### 2️⃣ **Data Preprocessing**
To clean and prepare the text data for analysis, the following steps were performed:
- **Tokenization**: Breaking text into words using `nltk`.
- **Lowercasing**: Converting all text to lowercase.
- **Stopword Removal**: Removing unimportant words like "the", "is", "a".
- **Lemmatization/Stemming**: Reducing words to their root form (e.g., "running" → "run").
- **Text Cleaning**: Removing special characters and unnecessary punctuation using `re.sub()`.

### 3️⃣ **Feature Engineering**
To represent text in a numerical format that machine learning models can process, we used:
- **TF-IDF (Term Frequency-Inverse Document Frequency)**: Assigns importance to words based on their frequency.
- **Bag-of-Words (CountVectorizer)**: Converts text into word occurrence matrices.
- **Word Embeddings**: Capturing semantic relationships between words.

### 4️⃣ **Model Training & Evaluation**
We implemented various machine learning models for classification:
- **Baseline Models:**
  - Most Frequent Label Classifier
  - Logistic Regression
- **Advanced Models:**
  - **Structured Perceptron**: Linear classifier for sequence-based tasks.
  - **LSTM (Long Short-Term Memory)**: Captures sequential text patterns.

**Evaluation Metrics:**
- **Accuracy, Precision, Recall, and F1-score** were used to measure performance.

### 5️⃣ **Results & Insights**
- The **LSTM model** outperformed traditional classifiers, demonstrating superior performance in distinguishing mental health categories.
- Exploratory Data Analysis (EDA) revealed insightful linguistic differences between mental health subreddits.
- The framework provides a foundation for **automated mental health monitoring and intervention**.

---

## 📂 Repository Structure
```
📂 Distinguishing_Mental_Health_NLP  
│── 📂 data               # Preprocessed and raw datasets  
│── 📂 notebooks          # Jupyter notebooks for EDA and model training  
│── 📄 README.md          # Project overview  
```

## 🔧 Installation & Usage

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/Distinguishing_Mental_Health_NLP.git  
   cd Distinguishing_Mental_Health_NLP  
   ```    
2. **Run the Jupyter notebook** for data processing and model training.

## 🔮 Future Scope
- Expanding the dataset to include more mental health-related subreddits.
- Using **transformer-based models (BERT, RoBERTa)** for improved text representation.
- Developing a real-time monitoring tool for mental health professionals.

## 📝 Acknowledgments
This project is part of my course **CIS 600: Applied Natural Language Processing** .

---
🚀 **Author:** Harshitha Kancher  
📧 [Email](mailto:harshithareddyk2002@gmail.com) | 🔗 [LinkedIn](https://www.linkedin.com/in/harshithareddyk)  

---


# 🧠 AI vs Human Text Classifier

This project is a simple **Machine Learning-based text classification system** that predicts whether a given text is **AI-generated or Human-written**.

It uses Natural Language Processing (NLP) techniques along with **TF-IDF Vectorization** and two classification models:

* Logistic Regression
* Naive Bayes

---

## 📌 Features

* Text preprocessing (lowercase + punctuation removal)
* TF-IDF vectorization
* Model training and evaluation
* Confidence-based decision layer
* Real-time user input prediction

---

## ⚙️ Technologies Used

* Python
* Pandas
* Scikit-learn

---

## 📂 Project Structure

```
├── dataset1.csv        # Dataset containing text and labels
├── main.py             # Main Python script
└── README.md           # Project documentation
```

---

## 📊 How It Works

### 1. Data Loading

The dataset is loaded using Pandas. It contains:

* `text` → Input sentence/paragraph
* `label` → AI or Human

### 2. Preprocessing

* Convert text to lowercase
* Remove punctuation

### 3. TF-IDF Vectorization

**TF-IDF (Term Frequency – Inverse Document Frequency)** converts text into numerical vectors.

* **Term Frequency (TF):** Frequency of a word in a sentence
* **Inverse Document Frequency (IDF):** Importance of the word across all documents

This helps in giving more importance to meaningful words and less to common words.

### 4. Model Training

Two models are trained:

* **Logistic Regression** → Linear classification model
* **Naive Bayes** → Probability-based model (works well for text)

### 5. Evaluation

Accuracy is calculated using test data to compare model performance.

### 6. Decision Layer

Based on prediction confidence:

| Confidence | Decision            |
| ---------- | ------------------- |
| ≥ 0.80     | Acceptable          |
| 0.60–0.79  | Needs Review        |
| < 0.60     | Likely AI-generated |

### 7. Prediction

User can input text and get:

* Prediction label
* Confidence score
* Decision output

---

## ▶️ How to Run

### Step 1: Install Dependencies

```bash
pip install pandas scikit-learn
```

### Step 2: Run the Script

```bash
python main.py
```

### Step 3: Enter Text

```
Enter text: This is a sample sentence
```

---

## 📈 Sample Output

```
Dataset Loaded Successfully

Logistic Regression Accuracy: 0.92
Naive Bayes Accuracy: 0.89

--- RESULT ---
Text: this is a sample sentence
Prediction: Human
Confidence: 0.87
Decision: Acceptable
```

---

## 🚀 Future Improvements

* Use deep learning models (LSTM, BERT)
* Improve dataset size and quality
* Add web interface using Flask/Streamlit
* Deploy as a web application

---

## 👨‍💻 Author

**Trailblazers**

---

## ⭐ Note

This project is built for learning purposes and demonstrates basic NLP and Machine Learning concepts in a simple and understandable way.

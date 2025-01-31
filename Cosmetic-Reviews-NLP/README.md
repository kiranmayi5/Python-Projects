# **NLP-Based Word2Vec Analysis on Cosmetic Reviews**

## 📌 **Project Overview**

This project applies **Natural Language Processing (NLP)** techniques to analyze **customer reviews** of cosmetic products from Nykaa. The focus is on leveraging **Word2Vec embeddings** to understand common themes in customer feedback, identify frequently mentioned terms, and uncover relationships between words in positive and negative reviews.

## 🎯 **Business Objective**

- Extract key product-related themes using **Word2Vec embeddings**.
- Identify the most common words in **positive vs. negative reviews**.
- Help brands understand customer sentiment by exploring word relationships.

## 🗂 **Dataset**

- **Source:** Kaggle (Nykaa cosmetic product reviews).
- **Data Format:** CSV file with columns like `Product Name`, `Review`, `Rating`, and `Date`.
- **Preprocessing:**
  - Tokenization and stopword removal
  - Lowercasing and punctuation removal
  - Lemmatization for better word representation

## 🔍 **Methodology**

### 1️⃣ **Data Preprocessing**

- Cleaned and tokenized text (removal of stopwords, special characters).
- Converted all text to lowercase for consistency.
- Applied **lemmatization** to enhance word representations.

### 2️⃣ **Word2Vec Training**

- Used **Gensim's Word2Vec** to train a model on customer reviews.
- Applied **skip-gram architecture (sg=1)** to capture word relationships.
- Tuned hyperparameters:
  - `vector_size=100`: 100-dimensional word embeddings
  - `window=5`: Context window size
  - `min_count=5`: Words appearing less than 5 times were ignored
  - `epochs=50`: Number of training iterations

### 3️⃣ **Findings & Insights**

- **Sentiment Trends**:
  - Reviews with a **rating of 4 and above** tend to use words like **"lovely", "superb", "beautiful", and "easy"**.
  - Negative reviews (ratings **2 and below**) commonly include words like **"worst", "waste", "disappointed", and "bad"**.

- **Sentiment Distribution Analysis**:
  - Certain **brands have a higher average sentiment score**, while some brands receive **consistent complaints about product quality**.
  - A trend of **seasonal variations** in customer sentiment was observed (e.g., **moisturizers** get more positive reviews in winter).

- **Word Relationships Identified Using Word2Vec**:
  - "moisturizer" is strongly associated with **"sunscreen"**, **"foundation"**, and **"cream"**

## 🛠 **Tech Stack**

- **Language:** Python
- **Libraries:** Gensim (Word2Vec), NLTK, Pandas, Matplotlib, Seaborn
- **Notebook:** Jupyter

## 📊 **Results & Visualizations**

- **Sentiment Score Trend Over Time**:
  - Plotted a **time-series visualization** of sentiment scores across months to track changes in customer satisfaction.

- **Top Positive & Negative Keywords**:
  - Identified and visualized the **most frequently used words** in high-rated vs. low-rated products using **bar charts**.

- **Word2Vec Word Embeddings**:
  - Used **t-SNE** to visualize word embeddings, showing clusters of similar words.
  - Example: **"foundation" and "coverage" are close together in vector space**.

- **Most Positive & Negative Brands**:
  - A **brand-wise sentiment score analysis** showed which brands are consistently rated highly and which ones receive negative feedback.

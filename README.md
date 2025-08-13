#  Dr.AnswerBot – Medical Question Answering Bot

An intelligent **Natural Language Processing (NLP)** bot designed to answer medical questions in simple, clear language.  
The bot uses text preprocessing, vector similarity, and machine learning models to understand user queries and provide accurate, knowledge-based responses.

---

##  Overview

**Dr.AnswerBot** acts as a medical learning assistant:
- Understands user questions in natural language.
- Retrieves and returns relevant medical knowledge.
- Uses pre-trained embeddings and ML models to improve answer accuracy.
- Can handle variations in phrasing and synonyms.

**Example interaction:**
User: What are the treatments for Nonalcoholic Steatohepatitis?
Bot: [Provides a detailed medically accurate answer...]


---

## System Architecture

### NLP Pipeline
1. **Text Preprocessing**
   - Tokenization (NLTK)
   - Stopword removal
   - Lowercasing & punctuation removal
2. **Feature Extraction**
   - TF-IDF Vectorization
   - Word Embeddings (Word2Vec via Gensim)
3. **Similarity Matching**
   - Cosine similarity to find most relevant answer
4. **Machine Learning Models**
   - Naive Bayes
   - Logistic Regression
   - GRU-based neural network (Keras/TensorFlow)
5. **Evaluation**
   - Accuracy, Precision, Recall, F1-score

---

## Technologies & Libraries
- **NLP**: NLTK, Gensim
- **ML Models**: scikit-learn, TensorFlow/Keras
- **Data Processing**: Pandas, NumPy
- **Vectorization**: TF-IDF, Word2Vec
- **Similarity Metrics**: Cosine Similarity
- **Visualization**: Matplotlib, Seaborn

-

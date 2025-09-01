# Medical Chatbot using NLP  

by **Shrouq Ahmad Aldalbahi***  

---

## Problem Statement  

The primary goal of this project is to develop an **NLP-based medical chatbot** capable of accurately answering a wide range of medical inquiries.  

- **Motivation**  
  - Improve healthcare accessibility by providing instant and reliable information.  
  - Bridge knowledge gaps where access to healthcare professionals is limited.  

- **Scope**  
  - Focuses on **text-based questions and answers**.  
  - Provides **credible responses** sourced from a trusted dataset.  

- **Expected Result**  
  - Deliver accurate and understandable responses to users’ medical queries.  

> ⚠️ Disclaimer: This chatbot is for **educational purposes only** and should not be considered medical advice.  

---

## Dataset  

- **Name**: MedQuAD – Medical Question Answering Dataset  
- **Size**: ~16,000 entries (questions, answers, source, focus area)  
- **Coverage**: 14,984 unique questions across diverse medical topics.  
- **Average**: ~1.1 answers per question (some up to 20 answers).  
- **Focus Areas**: Wide range of specialties such as cardiology, dermatology, oncology, etc.  

[[Dataset on Kaggle](https://www.kaggle.com/datasets/abhinavwalia95/medquad)](https://www.kaggle.com/datasets/pythonafroz/medquad-medical-question-answer-for-ai-research)  

---

## Preprocessing  

To prepare the dataset for similarity-based matching, the following steps were applied:  

- **Tokenization**: Split sentences into words.  
- **Normalization**: Lowercasing and punctuation removal.  
- **Lemmatization**: Reducing words to their base form (e.g., “running” → “run”).  
- **Stopword Removal**: Filtering out common words such as “the”, “and”, etc.  

These steps ensured that both user queries and dataset answers were represented in a **clean and consistent format**.  

---

## Text Representation  

For the chatbot to “understand” user queries, text was converted into numerical vectors.  

- **TF-IDF (Term Frequency – Inverse Document Frequency)**  
  - Used as the **primary method**.  
  - Transforms both medical questions and user queries into vectors.  
  - Cosine similarity is then used to find the closest matching question, and the corresponding answer is retrieved.  

- **Other methods explored**:  
  - Bag of Words (BoW)  
  - Word Embeddings (GloVe)  
  These were tested but not included in the final workflow to keep the system lightweight.  

---

## Chat Flow  

The chatbot’s logic:  

1. Preprocess user input.  
2. Convert query and stored questions into TF-IDF vectors.  
3. Compute **cosine similarity**.  
4. Retrieve the **answer** linked to the most similar question.  

### Example Interaction  
User: What are the symptoms of diabetes?
Bot: The most common symptoms of diabetes include frequent urination, excessive thirst, unexplained weight loss, and fatigue.



---

## References  

- [[MedQuAD: Medical Question Answering Dataset – Kaggle](https://www.kaggle.com/datasets/abhinavwalia95/medquad)  ](https://www.kaggle.com/datasets/pythonafroz/medquad-medical-question-answer-for-ai-research)
- Bhavsar, S. (2021). *Building a Chatbot in Python*. datamahadev.com.  
- Hickman, L., Thapa, S., Tay, L., Cao, M., & Srinivasan, P. (2022). *Text preprocessing for text mining in organizational research: Review and recommendations.* Organizational Research Methods, 25(1), 114-146.  
- Intellipaat (YouTube). *Building Chatbots with Python*.  


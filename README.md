
# Hate Speech Detection in Indonesian Using NLP

This project aims to detect hate speech in Indonesian social media using Natural Language Processing (NLP) techniques. It focuses on building models that classify text as hate speech or non-hate speech, contributing to a safer online environment.

## Team Members
- **Yendri Kilauan Purnama** - Data Analyst
- **Banu Salman Farisi** - Data Analyst
- **Adhitama Ihza Pangestu** - Data Analyst

## Table of Contents
1. [Project Overview](#project-overview)
2. [Problem Statement](#problem-statement)
3. [Data](#data)
4. [Methodology](#methodology)
5. [Results](#results)
6. [Insights](#insights)
7. [Next Steps](#next-steps)

## Project Overview
Hate speech on social media platforms can lead to real-world harm, including fostering discrimination, violence, and psychological damage. This project aims to automatically detect hate speech in Indonesian-language tweets, helping platforms flag and manage harmful content efficiently.

## Problem Statement
The rise of hate speech on social media has serious implications, including discrimination and violence. This project addresses the need for automatic detection systems that help social media platforms manage content more effectively.

## Data
The dataset consists of Indonesian-language tweets, labeled as either hate speech or non-hate speech. 

### Data Preprocessing
The data underwent several preprocessing steps:
1. **Filtering**: Removal of numbers, retweets, hashtags, hyperlinks, punctuation, and emoticons.
2. **Tokenization**: Using `TweetTokenizer` and `stopwords_indonesia`.
3. **Stemming**: Using the `Sastrawi` stemmer.
4. **TF-IDF**: Applying `CountVectorizer` and `TfidfTransformer` for feature extraction.

## Methodology
The project utilized the following techniques and tools:
- **Exploratory Data Analysis (EDA)**: To understand data distribution and label counts.
- **Text Processing**: Filtering, tokenization, stemming, and applying TF-IDF for vectorization.
- **Algorithms**:
  - **Naive Bayes**
  - **Support Vector Machine (SVM)**
  
### Hyperparameter Tuning
Both models were fine-tuned using `GridSearchCV` to optimize their performance.

### Evaluation Metrics
- **Accuracy**
- **Precision**
- **Recall**
- **F1-Score**

## Results
The project compared the performance of Naive Bayes and SVM, with the following results:

- **Naive Bayes Accuracy**: 96.69%
- **SVM Accuracy**: 96.62%

Naive Bayes slightly outperformed SVM in this task.

## Insights
- Both algorithms were able to distinguish between hate speech and non-hate speech effectively.
- Hyperparameter tuning with `GridSearchCV` significantly improved the model performance.
- **Naive Bayes** performed slightly better than SVM in terms of accuracy.

## Next Steps
- Experiment with different algorithms to further enhance the model performance.
- Improve existing models by incorporating additional data or more advanced techniques.
- Create a user interface where new sentences can be tested for hate speech detection.

## How to Run the Project

### Prerequisites
- Python 3.x
- Required Libraries:
  - `pandas`
  - `nltk`
  - `sklearn`
  - `sastrawi`

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/hate-speech-detection-nlp.git
   ```
2. Install the required libraries:
   ```bash
   pip install -r requirements.txt
   ```
3. Run the model training:
   ```bash
   python train_model.py
   ```
4. Test the model with new input:
   ```bash
   python test_model.py
   ```

## Acknowledgments
A special thanks to all team members for their collaboration, and to the open-source community for providing the libraries used in this project.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

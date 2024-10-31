# StackOverflow-Tag-Prediction

### Description
Stack Overflow is the largest and most trusted online community for developers to learn, share knowledge, and advance their careers. Each month, over 50 million developers use the platform to seek answers and contribute insights across a wide range of programming topics.

### Problem Statemtent
Suggest tags based on the content of questions posted on Stack Overflow.

### Constraints
There are no strict latency constraints.

## About Data Set
1. The dataset is in CSV format.
2. It contains two columns: title and tags.
3. The dataset consists of a total of 100,000 rows.
4. Each row represents a question and its corresponding tags.

## Machine Learning Problem
It is a multi-label classification problem. This means we assign multiple labels to each sample, so a single data point can have several relevant properties.

For example, a Stack Overflow question might relate to topics like Python, Web Development, APIs, or Data Science simultaneously.

## Performance metric
Micro-Averaged F1-Score (Mean F Score): The F1 score is like a balanced average of precision and recall, giving equal weight to both. It ranges from 0 to 1, with 1 being the best score and 0 the worst.

F1 = 2 * (precision * recall) / (precision + recall)

## Exploratory Data Analysis (EDA)
### Load Data
• Using Pandas to load the CSV file into a DataFrame.
### Checking for duplicates and missing values
• There are no duplicates rows in the dataset.

• There are no missing values in the dataset.
### Most frequently and Least frequently occurring tag
• JavaScript is the most repeated tag, appearing 19,078 times.

• Mongodb is the least repeated tag, appearing 350 times.

• Since some tags occur much more frequenctly than others, Micro-averaged F1-score is the appropriate metric for this problem.
### Unique Tags
• There are a total of 100 unique tags in the dataset.

## Tags Per Question
• Maximum number of tags per question: 4

• Minimum number of tags per question: 1

• Avg number of tags per question: 2.183

• Most of the questions are having 2 or 3 tags

## Data cleaning and preprocessing
• Remove Spcial characters from title.

• Remove stop words.

• Remove HTML Tags.

• Convert to lower case.

• Use SnowballStemmer to stem the words.

• Converting Text (Title) to Vector Using TF-IDF Vectorizer
## Training Machine Learning Model
### Train Test Split
• Splitting 80% data into train and 20% data into test using random split.
### MultinomialNB with OneVsRest Classifier
• F1 score - 0.7983 ~ 0.8
### Logistic Regression with OneVsRest Classifier
• F1 score - 0.7426
### Linear SVM with OneVsRest Classifier
• F1 score - 0.7380
### KNN with OneVsRest Classifier
• F1 score - 0.7165
## Result
![Screenshot 2024-10-31 091848](https://github.com/user-attachments/assets/fd371481-96d5-4565-871a-2116be14fce4)

https://github.com/user-attachments/assets/6b68908d-905e-4575-a63b-0988c031021f

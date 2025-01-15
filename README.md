# Application of Naive Bayes to Sentiment Analysis of Text

## Project Overview
This project was completed as part of the **CSCI-3613 Artificial Intelligence** course, which focuses on various machine learning techniques and their applications.

This project applies the Naive Bayes algorithm to perform sentiment analysis on text data, specifically using the Cornell Movie Review dataset. The analysis includes two main implementations:
1. **Manual Implementation**: The Naive Bayes algorithm is implemented from scratch.
2. **Library Implementation**: The Naive Bayes algorithm is applied using the `MultinomialNB` classifier from the `scikit-learn` Python library.

The dataset consists of 1000 positive and 1000 negative movie reviews.


## Instructions

### Dataset Citation

The dataset used in this project is the Cornell Movie Review dataset:
[polarity dataset v2.0](https://www.cs.cornell.edu/people/pabo/movie-review-data/review_polarity.tar.gz) ( 3.0Mb) (includes [README v2.0](https://www.cs.cornell.edu/people/pabo/movie-review-data/poldata.README.2.0.txt)): 1000 positive and 1000 negative processed reviews. Introduced in Pang/Lee ACL 2004. Released June 2004.

For more details, visit [Cornell's Movie Review Data Page](http://www.cs.cornell.edu/people/pabo/movie-review-data/).



### Data Preparation and Preprocessing
1. Load the reviews from the dataset and label them as 'positive' or 'negative'.
2. Convert the dataset into a DataFrame for easier manipulation.
3. Preprocess the data by:
   - Removing non-alphanumeric characters.
   - Tokenizing the reviews into words.
   - Removing stopwords.

### Manual Implementation
- Implement the Naive Bayes algorithm from scratch.
- Split the dataset into training (80%) and testing (20%) sets without a fixed random seed for unbiased evaluation.
- Use token frequencies to calculate probabilities for classification.
- Generate a classification report showing precision, recall, and F1-score for both classes.

### Library Implementation
- Utilize `CountVectorizer` from `scikit-learn` to convert text data into token counts.
- Train the `MultinomialNB` classifier on the training set.
- Evaluate the model using the test set.
- Generate accuracy and classification reports.

## Analysis
- Compare the performance of manual and library implementations.
- Discuss the differences in results, including accuracy, precision, and recall, and attribute them to factors like numerical precision, tokenization methods, and optimization in library-based models.

## Requirements
- Python 3.x
- `scikit-learn`
- `pandas`
- `nltk`

## Running the Project
1. Install the required Python packages.

2. Open the .pynb file in Jupyter Notebook or any compatible environment.

3. Specify the download directory for NLTK stopwords in your code as follows: 
`nltk.download('stopwords', download_dir=r'C:\Users\aze\Desktop\application_of_Naive_Bayes')`

4. Update the path in your code to load the reviews:
`reviews, labels = load_reviews(r'C:\Users\aze\Desktop\application_of_Naive_Bayes\txt_sentoken')
`

5. Run the notebook cells sequentially to execute the preprocessing, manual implementation, and library implementation steps.


## Conclusion
- The library-based implementation showed higher accuracy and balanced performance, attributed to the optimizations inherent in established machine learning libraries. 
- The manual implementation, while slightly less accurate, served as a valuable educational tool to understand the Naive Bayes algorithm's mechanics.


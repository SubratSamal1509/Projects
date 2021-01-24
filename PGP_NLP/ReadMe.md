## Toxicity

Using NLP and machine learning, make a model to identify toxic comments from the Talk edit pages on Wikipedia. Help identify the words that make a comment toxic.

#### Problem Statement:  

Wikipedia is the world’s largest and most popular reference work on the internet with about 500 million unique visitors per month. It also has millions of contributors who can make edits to pages. The Talk edit pages, the key community interaction forum where the contributing community interacts or discusses or debates about the changes pertaining to a particular topic. 

Wikipedia continuously strives to help online discussion become more productive and respectful. You are a data scientist at Wikipedia who will help Wikipedia to build a predictive model that identifies toxic comments in the discussion and marks them for cleanup by using NLP and machine learning. Post that, help identify the top terms from the toxic comments. 

#### Domain: Internet

Analysis to be done: Build a text classification model using NLP and machine learning that detects toxic comments.

#### Content: 

id: identifier number of the comment

comment_text: the text in the comment

toxic: 0 (non-toxic) /1 (toxic)

#### Steps Performed:

Cleanup the text data, using TF-IDF convert to vector space representation, use Support Vector Machines to detect toxic comments. Finally, get the list of top 15 toxic terms from the comments identified by the model.


Load the data using read_csv function from pandas package

- Get the comments into a list, for easy text cleanup and manipulation

- Cleanup: Using regular expressions, remove IP addresses, remove URLs

- Normalize the casing, Tokenize using word_tokenize from NLTK

- Remove stop words,  Remove punctuation

- Find the top terms in the data and check for contextual stop words

- Use TF-IDF values for the terms as feature to get into a vector space model

- Import TF-IDF vectorizer from sklearn

- Model building: Support Vector Machine

- Model evaluation: Accuracy, recall, and f1_score
 
- The model seems to focus on the 0s, Hyperparameter tuning

- Import GridSearch and StratifiedKFold (because of class imbalance)

- Find the parameters with the best recall in cross validation

- Predict and evaluate using the best estimator

- Use best estimator from the grid search to make predictions on the test set

- What are the most prominent terms in the toxic comments

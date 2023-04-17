# NewSNLP
This code performs a text classification task using three different machine learning algorithms: K-Nearest Neighbors (KNN), Multinomial Naive Bayes (Multi NB), and Random Forest. The data is stored in a CSV file named "news.csv" and contains news articles with their sources.

First, the code reads the CSV file and drops the 'published_at' and 'topic' columns, as they are not relevant for the classification task. Then, it checks the dimensions of the dataframe and removes any rows with missing or NaN values and duplicates. The dataframe is then filled with the mean, median, or mode of the remaining values to handle any remaining missing values.

Next, the code splits the data into training and test sets, with 10% of the data reserved for testing. The training and test data are split into the content (news articles) and the source (news source) for use in the classification task.

Three machine learning algorithms are used for classification: KNN, Multi NB, and Random Forest. Each algorithm is implemented using a pipeline that first transforms the data using TfidfVectorizer, a method for text feature extraction, and then fits the transformed data to the machine learning algorithm.

After fitting the training data to each algorithm, the code predicts the test data and prints the classification report for each algorithm. The classification report includes precision, recall, f1-score, and support for each class (news source) and an overall accuracy score for the algorithm.

Finally, the code uses Spacy to preprocess the text by removing stop words and lemmatizing the text. The preprocessed text is stored in a new column called 'New_Content'. The code then repeats the model building with the newly preprocessed text, and prints the classification report and confusion matrix for the Random Forest algorithm.

Overall, this code performs a text classification task using three different machine learning algorithms and demonstrates how pre-processing can improve the accuracy of the model.

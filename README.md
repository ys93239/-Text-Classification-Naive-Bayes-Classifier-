Scalable Document Classification
--------------------------------

Team Name: DAYS

Team Members:
- Yash Shrivastava
- Dharamendra Prajapati
- Sharmin Pathan

Technologies Used:
- Spark Core
- Spark SQL
- Resilient Distributed Datasets (RDDs)
- DataSets
- Java 1.8

Preprocessing:
The training subsets are filtered for removal of
- stopwords: A properties file that contains a list of stopwords that don't contribute to the classification process like articles, prepostions, etc
- special characters

Vocabulary List:
After filtering the training subsets, a vocabulary has been built for the classification process.

Classification Process:
Naive Bayes Classifier has been applied.
Probabilities of every word appearing in the vocabulary list against every document and the category label assigned for that document is calculated. The documents and category label probabilities have also been computed.
The classifier on being applied to the testing subsets, gives its classification category.

Smoothing:
Applied to the testing subsets to avoid the worst case of 0 probability for a word that appears in the testing subsets but was not in the training subset.

Flow:
The program takes the following 5 arguments as inputs
arg0 = location of test input file 
arg1 = location of classifer file
arg2 = loaction of vocabulary probablity file
arg4 = specify the mode whether its the training or testing mode
arg5 = location of output file


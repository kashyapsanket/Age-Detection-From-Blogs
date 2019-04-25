The Blog Authorship corpus is the set of blogs available on blogger.com in 2004. In this paper, we try
to predict the age category of the blog author depending on the textual content and writing style of the
author. We first extract features at varying granularity (sentence, word, character) to create a feature set
which is then used for classification. The size of the feature set is 88 elements which are a combination of
the above discussed features. We observe multiple classifiers (SVM, Random Forest, XGBoost etc.) and
finally see that the Multi-Layer Perceptron classifier performs the best, giving an accuracy of 72.83%.

Data
The Blog Authorship corpus has the post data for 19,320 bloggers, in an .xml file for each blogger. The data
is first cleaned of non-unicode characters and each blogpost is saved as a row of the given dataframe, ['ID',
'Gender', 'Age', 'Industry', 'Sign', 'Date', 'Text']. The models are trained to predict the 'Age' parameter.
The problem is posed as a multi-class classification problem not a regression problem where we predict the
exact age of the blog author so the 'Age' variable is converted to a categorical label.




# Sentiment Analysis 

Author: Naila Thevenot

Date: Fall 2022

### Abstract

Using a combination of built-in Python library and my own functions, I devised a program to do sentiment analysis. Using Twitter data, the model can classify whether or not the sentiment is positive, negative, uncertain, or litigious. 

To prep the data to be usable by an ML algorithm like Support Vector Machines I clean the data by using libraries to convert emojies, and emoticons to words. They aren't in a format usable by an algorithm but they give a lot of insight about the tone of the text. 

Next, I remove stopwords which are words that to not add much value to the semantics of a language for example "is, the, are". Following this, I "stem" the words which means that I standardize the form of the word so that for example "singing, sing" are not evaluated as different words. Keeping the text as is, would be more compuatational expensive for marginal benefits. 

The last feature engineering step that I take is to use CountVectorizer to create n-grams. That way the words in the data set are all considered features for each example (row). The benefit of n-grams as opposed to bag-of-words is that with n-grams you can choose sequences of words to be the feature set. For example as opposed to a feature set consisting of [he, is, the, king], with an n-gram of two, you would have [he is, is the, the king]. That way the context of the word is better preserved. 

Finally, I use an SVC algorithm to classify the sentiment of the data, followed by other algorithms to gage the results across different classification algorithms. 


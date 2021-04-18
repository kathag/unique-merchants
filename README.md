# unique-merchants
In the corpus, find the total number of unique merchants and their frequency of occurrence. 


#Approach
Efficiently groups similar values in large (or small) datasets. it builds a document term matrix of n-grams assigned a TF-IDF score. It then uses matrix multiplication to calculate the cosine similarity between these values. 

# How do I use it?
This Project have a python3 notebook for source code. 
```
Dependencies:
 - pandas
 - scikit-learn
 - scipy
 - numpy
```
Project Contains Matcher class, which calculates tf-idf scoring and cosine similarties.

```
Matcher((df, columns_to_group, match_threshold=0.75, ngram_remove=r'[,-./]', ngram_length=3))
```

## Class parameters:

* df (required): A Pandas' DataFrame containing the dataset to group
* columns_to_group (required): A list or string matching the column header(s) you'd like to parse and group
* match_threshold (optional): This is a floating point number between 0 and 1 that represents the cosine similarity threshold we'll use to determine if two strings should be grouped. The closer the threshold to 1, the higher the similarity will need to be to be considered a match.
* ngram_remove (optional): A regular expression you can use to filter characters out of your strings when we build our n-grams.
* ngram_length (optional): The length of our n-grams. This can be used in tandem with match_threshold to find the sweet spot for grouping your dataset. If TextPack is running slow, it's usually a sign to consider raising the n-gram length.

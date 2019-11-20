# PyData -- 2017
- We have to find the definision of what similarity means if shore and coast are similar  the clothes and closet also similar in the case they are really related
- We can say that the simialr words are different because they are not interchangable
- Inorder to find the modet similar words that mean which are interchangable 
- Steps
- First import the dataset
- preprocess it and convert it to list of sentences
- feed it to the genism model along with the window parameter
- After training it the model can be called with most_similar() and the parameter can be the word which we have to find the similarity
- The window parameter is the neighbourhood like if we define the window parameter as 2 then we go to the left 2 and the right 2
- If two words in the window seems in a frequent manner the more similar they become
- When the window size is more than 50  then it will consider the entire sentence and which will give a broad consideration to the similar words
- We have to check the word2vec work for the interchangable or not - this is the case where word2vec is not work
- We have to analyse our dataset for our use case and then proceed
- If we are using different embedding the result will be different - the word rank will give you the attribute and word2vec will give you the interchangable words and fasttext will give you a mix of both
- gensim has a api to fasttext also and looks exaclty like the word2vec
- fasttext is written in c++ and it is slow to word2vec
## Theory of word embedding
- The simplest method is one hot encoder where each word is represented with 1 according to a positoin
- In this method there is no relationship between the words
- In PCA the words are similar are put close and if the words are faar away they are put faar apart
- The co occurance matrix are informative but they are pretty big as the size of the vocabulary
- Then we use a dimentionality redution then the firt matrix u will gives the embedding for the first element
- U is the word embedding and V is the context the dot product of them will give the co occurance count
- In the case of fasttext they are considering not only the words as well as the sub words
- And the similarity score in the fast text is the sum of dot product of all word embedding U and context embedding V
### Word rank 
- when the context word is given it will return a list of words from the corpus where the first one will be the most similar and last one will be a less one
- So the whole idea is like 
- if we want to find the similarity
- related similarity and if we have corpus > 1M
- Then use word to vec 
- else use wordrank
- interchangable similarity then use fasttext , word2vec , varembedd
- Note: before training if we are labeling the can/n and can/vb which indicate the can as a noun and verb respectively then at that case we get different embedding for can - it is a easy method using spacy if we have to find out the words with multiple meaning
- The engineering aspect of glove makes it difficult to process is that glove will process the entire corpus and the co-occurance matrix have to be stored in the memory but in the case of word2vec the co-occurance matrix is created as a streaming fashion
- The dimension parameter in the function is entirely a machine learning thing that is the dimension is big mean it may cause the over fitting and if the dimension is small it cause the underfitting
# Doc2vec and machine learning classification


- The input is a word as a one hot vector
- predict the next word - according to the the probability of the word
- There is two matrix of weights like w context and w word
- according to the representation in the one hot it will extract the row from the w context
- at the output layer we will use softmax and will give the probability of the word on the other all vectors
- probability is the proportional to the dot product between jth column of W context and ith column of the word  
- for the next time the two words are considered and then the weight matrix corresopoding to that two indexes are retrieved
- the summed up and fed into the w word and the to the softmax
- By softmaz the weights for the corresponding word will change in word context and all weight will be updated 
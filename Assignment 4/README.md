## Bi-directional stacked RNN with GRU

Repeat Assignment 3 (text classification with MLPs), now using a bi-directional
stacked RNN (with GRU or LSTM cells) implemented (by you) in Keras/TensorFlow or
PyTorch. Tune the hyper-parameters (e.g., number of stacked RNNs, dropout probability) on
the development subset. Monitor the performance of the RNN on the development subset
during training to decide how many epochs to use. You may optionally add an extra RNN
layer to produce word embeddings from characters, concatenating each
resulting character-based word embedding with the corresponding pre-trained word
embedding (e.g., obtained with Word2Vec). You may optionally add a pre-trained language
model as an extra layer to obtain context-sensitive word embeddings. 
Include experimental results of a baseline that tags each word with the most
frequent tag it had in the training data; for words that were not encountered in the training
data, the baseline should return the most frequent tag (over all words) of the training data.


Also include experimental results of your best method of Assignment 3 (if you chose
that exercise), now treated as an additional baseline. Include in your report:

• Curves showing the loss on training and development data as a function of epochs.

• Precision, recall, F1, precision-recall AUC scores for each class (tag) and classifier,
separately for the training, development, and test subsets.

• Macro-averaged precision, recall, F1, precision-recall AUC scores for each classifier,
separately for the training, development, and test subsets.

• A short description of the methods and datasets you used, including statistics about
the datasets (e.g., average document length, number of training/dev/test documents,
vocabulary size) and a description of the preprocessing steps that you performed

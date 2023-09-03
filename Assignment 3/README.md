## Repeat Assignment 2 (text classification with mostly linear classifiers), but now using
## an MLP classifier implemented (by you) in Keras/TensorFlow or PyTorch.

You may use different features in the MLP classifier than the ones you used in Assignment 2.
Tunethe hyper-parameters (e.g., number of hidden layers, dropout probability) on the development
subset of your dataset. Monitor the performance of the MLP on the development subset
during training to decide how many epochs to use. Include experimental results of a baseline
majority classifier, as well as experimental results of your best classifier from Assignment 2,
now treated as a second baseline. Include in your report:

• Curves showing the loss on training and development data as a function of epochs.

• Precision, recall, F1, precision-recall AUC scores, for each class and classifier,
separately for the training, development, and test subsets, as in Assignment 2.

• Macro-averaged precision, recall, F1, precision-recall AUC scores (averaging the
corresponding scores of the previous bullet over the classes), for each classifier,
separately for the training, development, and test subsets, as in Assignment 2.

• A short description of the methods and datasets you used, including statistics about
the datasets (e.g., average document length, number of training/dev/test documents,
vocabulary size) and a description of the preprocessing steps that you performed.

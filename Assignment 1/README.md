## Bigram & Trigram Language Model

Implement a bigram and a trigram language model for sentences, using Laplace smoothing.
In practice, n-gram language models compute the sum of the logarithms of the n-gram probabilities of each sequence,
instead of their product and you should do the same. Assume that each sentence starts with the pseudo-token
*start* (or two pseudo-tokens *start1*, *start2* for the trigram model) and ends with the
pseudo-token *end*. Train your models on a training subset of a corpus (e.g., a subset of a
corpus included in NLTK – see http://www.nltk.org/). Include in the vocabulary only words
that occur, e.g., at least 10 times in the training subset. Use the same vocabulary in the bigram
and trigram models. Replace all out-of-vocabulary (OOV) words (in the training,
development, test subsets) by a special token *UNK*. Alternatively, you may want to use
BPEs instead of words (obtaining the BPE vocabulary from your training subset) to avoid
unknown words. See Section 2.4.3 (“Byte-Pair Encoding for Tokenization”) of the 3rd edition
of Jurafsky & Martin’s book (https://web.stanford.edu/~jurafsky/slp3/); for more information,
check https://huggingface.co/transformers/master/tokenizer_summary.html.
                                  
(ii) Estimate the language cross-entropy and perplexity of your two models on a test subset of
the corpus, treating the entire test subset as a single sequence of sentences, with *start* (or
*start1*, *start2*) at the beginning of each sentence, and *end* at the end of each sentence.
Do not include probabilities of the form P(*start*|…) or P(*start1*|…), P(*start2*|…) in the
computation of cross-entropy and perplexity, since we are not predicting the start pseudotokens; but include probabilities of the form P(*end*|…), since we do want to be able to
predict if a word will be the last one of a sentence. You must also count *end* tokens (but not
*start*, *start1*, *start2* tokens) in the total length N of the test corpus.
                                  
(iii) Develop a context-aware spelling corrector (for both types of errors) using your
bigram language model, a beam search decoder, and the formulae.
If you are very keen, you can also try using your trigram model.
You can use the inverse of the Levenshtein distance. 
                                                  
(iv) Create an artificial test dataset to evaluate your context-aware spelling corrector. You
may use, for example, the test dataset that you used to evaluate your language models, but
now replace with a small probability each non-space character of each test sentence with
another random (or visually or acoustically similar) non-space character (e.g., “This is an
interesting course.” may become “Tais is an imterestieg kourse”).
                                                  
(v) Evaluate your context-aware spelling corrector in terms of Word Error Rate (WER) and
Character Error Rate (CER), using the original (before character replacements) form of your
test dataset of question (iv) as ground truth (reference sentences), and averaging WER (or
CER) over the test sentences. CER is similar to Word Error Rate (WER), but operates at the
character level

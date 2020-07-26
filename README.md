# Auto-Peotry-Genrating-using-NLP

The task is to generate a poem using different models. We will generate a poem verse by verse until all four
stanzas have been generated. The poetry generation problem can be solved using the following steps:<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 1: Load the Gutenberg Poetry Corpus<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 2: Tokenize the corpus in order to split it into a list of words<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 3: Generate ngram models<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 4: For each of the four stanzas<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; - For each verse<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; i: Generate a random number between 5 and 10<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;ii: Select first word<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; iii: Select subsequent words until end of verse<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;iv: If not the rst verse, make sure the last word rhymes with the previous verse<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; v: Print verse<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- Print empty line after stanza<br/>

## Main Challenges
Among the challenges of solving this task the selection of subsequent words once we have chosen
the first word of the verse. But, in order to predict the next word, what we really want to compute is what is
the most likely next word out of all of the possible next words. In other words, find the word that occurred the
most often after the condition in the corpus. We can use a Conditional Frequency Distribution (CFD) to figure
that out! A CFD can tell us: given a condition, what is likelihood of each possible outcome.
Rhyming verses is also a challenge. CMUDict is a pronunciation dictionary which can be used to match the last
syllable of each verse after the first.
## Standard n-gram Models
In this task we will train a unigram model, a bigram model and a trigram model for generating a four-line sonnet.
We can develop our model using the Conditional Frequency Distribution method. First develop a unigram model
(UniGram) and then the bigram model (BigramModel). Select the First word of each line randomly from the
high frequency words in the vocabulary and then use the bigram model to generate the next word until the verse
is complete. Generate the next three lines similarly. Follow the same steps for the trigram model and compare
the results of the two n-gram models. Can we make the sonnet rhyme? (Hint: use a pronunciation dictionary
such as CMUdict)
## Backward Bigram Model
Standard n-gram language models model the generation of text from left to right. However, in some cases, tokens
might be better predicted from their right context rather than their left context.
The next task is to produce a backward bigram model that models the generation of a sentence from right to left.
Think of a very simple way to very quickly use BigramModel to produce a BackwardBigramModel that is
identical except for the modeling direction. Compare the results of the backward bigram model with previous
implementations.
## Bidirectional Bigram Model
Next build a BidirectionalBigramModel that combines the forward and backward model. Both the Back-
wardBigramModel and BidirectionalBigramModel should take the same input and produce the same style
of output as BigramModel. Compare the output with the previous models.
### Perplexity
Can we measure how good our generated poetry is from dierent models? Calculate the Perplexity of each
model.

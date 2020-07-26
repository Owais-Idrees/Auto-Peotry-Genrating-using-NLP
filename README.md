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

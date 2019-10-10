# Kazakh-language-spelling-correction-and-lexical-analysis
1. Spelling correction : kazakh is an agglutinative language that belongs to the Turkic
group. It has a complex and productive derivational and inflectional morphology.
While extensive research has been conducted into the morphological analysis of
agglutinative languages, not too much work has been accomplished in building tools
for the analysis of Kazakh. Being one of the oldest problems in NLP with arguably the
highest demand for a practical solution, automatic spelling correction is one of the
basic steps in the analysis of any language. 

The spelling correction can be divided
into two tasks: word recognition and error correction. For languages with a fairly
straightforward morphology recognition may be reduced to a trivial dictionary look up:
if a given word is absent from the dictionary, then most likely it had been misspelled.
Correction is done through generating a list of possible suggestions: usually words
within some minimal edit distance to a misspelled word. 

For agglutinative languages,
such as Kazakh, even recognizing misspelled words becomes challenging as a
single root may produce hundreds of word forms. 

There is an instrument which helps
to make morphological analysis of the language called Apertium.

​ Apertium is a free/open-source machine translation platform. 

My solution replaces simple dictionary
lookup method by checking the right word form using Apertium. Here you can see the
corpus which was used by kazakh linguists creating kazakh grammar for apertium.
The second step is performed by scanning kazakh language corpus overall and
using dynamic programmings approach called the Levenshtein distance.
Mathematically, the Levenshtein distance between two strings a, b (of length |a| and
|b| respectively) is given by leva,b(|a|,|b|) where:

2. The configuration of the suggestions can be tuned easily, according to your needs.
Corpus can be found in ./KazakhCorpus section


3. Lexical analysis aim is to try to understand deeply the structure of kazakh language.
It scans through the whole data and extracts part of speech category from word and
also scans for mistakes at the same time. After this analysis we are able to extract
the most popular n-grams, count the number of errors and a lot of things restricted
only to your imagination. Extraction of speech categories is made by morphological
and lexical grammar described in KazakhGrammar.txt file in the root directory of the
project

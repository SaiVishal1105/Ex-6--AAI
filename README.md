<H3>ENTER YOUR NAME: SAI VISHAL D</H3>
<H3>ENTER YOUR REGISTER NO.: 212223230180</H3>
<H3>EX. NO.6</H3>
<H3>DATE: 26.10.2024</H3>
<H1 ALIGN =CENTER>Implementation of Semantic ANalysis</H1>

## Aim :

To perform Parts of speech identification and Synonym using Natural Language Processing (NLP) techniques.
 
## Algorithm :

### Step 1 :

Import the nltk library

### Step 2 :

Download the 'punkt', 'wordnet', and 'averaged_perceptron_tagger' resources.

### Step 3 :

Accept user input for the text.

### Step 4 :

Tokenize the input text into words using the word_tokenize function.

### Step 5 : Iterate through each word in the tokenized text.<br>
•	Perform part-of-speech tagging on the tokenized words using nltk.pos_tag.<br>
•	Print each word along with its corresponding part-of-speech tag.<br>
•	For each verb , iterate through its synsets (sets of synonyms) using wordnet.synsets(word).<br>
•	Extract synonyms and antonyms using lemma.name() and lemma.antonyms()[0].name() respectively.<br>
•	Print the unique sets of synonyms and antonyms.

## Program :

```
import nltk
#import wordnet
nltk.download( 'punkt' )
nltk.download('wordnet')
from nltk.tokenize import word_tokenize
nltk.download( 'averaged_perceptron_tagger' )
sentence=input ()
# Tokenize the sentence into words
words = word_tokenize(sentence)
# Identify the parts of speech for each word
pos_tags= nltk.pos_tag(words)
from nltk.corpus import wordnet

# Identify synonyms and antonyms for each word
synonyms =[]
antonyms =[]
for word in words:
	for syn in wordnet.synsets(word) :
		for lemma in syn.lemmas():
			synonyms . append (lemma . name( ) )
			if lemma . antonyms():
				antonyms . append ( lemma. antonyms ( ) [0] . name ( ) )
# Print the synonyms and antonyms
print ( "Synonyms : " ,set (synonyms) )
print ( "Antonyms : " ,set(antonyms) )

```

## OUTPUT :

![image](https://github.com/user-attachments/assets/923a3741-4f73-4497-a343-65306720fc09)


## Result :

Thus ,the program to perform the Parts of Speech identification and Synonymis executed sucessfully.

## Similar Words or Synonyms
The words like 'find' or 'search' are called synonyms and the project is to find all such synonyms from the text with the help of **WordNet**.

## [WordNet](https://wordnet.princeton.edu)
- WordNet was first created in English only in the Cognitive Science Laboratory of Princeton University under the direction of psychology professor **George Armitage Miller**
starting in 1985 and has been directed in recent years by **Christiane Fellbaum.**
- WordNet is a large lexical database of English. 
- It consist of noun, verb, adjective and even synonyms and antonyms of the words.
- We can consider it as a **Thesaurus**.
- Synsets are interlinked by means of conceptual-semantic and lexical relations.
- WordNet's structure makes it a useful tool for computational linguistics and Natural Language Processing.

## Synsets
- Synsets are also called Synonyms Ring.
- It is a set of one or more synonyms that are interchangable in the context of the language.
```py
>>> wordnet.synsets('win')
[Synset('win.n.01'),
 Synset('winnings.n.01'),
 Synset('win.v.01'),
 Synset('acquire.v.05'),
 Synset('gain.v.05'),
 Synset('succeed.v.01')]
```

## The Project Flow
- The previous given inputs or the new inputs are stored and passed on in the project flow.
- The text may contains many unwanted data with respective to English Vocabulary - Synonyms like numbers, punctuations marks and even uppercases.
- To remove them Regex or Regular Expressions are used 
```py
text = re.sub(r'[^a-zA-Z\s]+', '', text)
text = text.lower()
```
- Next is to remove the Stopwords(is, I, are, am, and, the) and tokenize to segregate the words.
- Next part is to **Lemmatization**.
- Lemmatization is the process of removing infectional endings and convert to base form or dictionary form of the word which is known as lemma.
- Coming to the last part of the project is taking the synsets of the lemmatized words.
- Here the output 

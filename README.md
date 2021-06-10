# madlib-spam-attack-BERT
This repo holds code and materials used in the paper **"Tackling Mad-lib Spam Attacks using BERT Encoding"**.

---

![Spam picture](https://cdn.pixabay.com/photo/2018/08/10/15/39/email-3597087_960_720.jpg)

## Brief overview

One of the stratagems used to deceive spam filters is to substitute vocables with synonyms or similar words that turn the message unrecognisable by the detection algorithms. We explore whether the recent development of language models sensitive to the semantics and context of words, such as Google's BERT, may be useful to overcome this adversarial attack, that we called "Mad-lib", as per the word substitution game. 

For this purpose we implemented two experiments using the SMS Spam Collection Dataset. In the first experiment we evaluated the performance of the widely known BoW and TFIDF document representation models and the novel BERT model, coupled with a variety of classification algorithms (Decision Tree, kNN, SVM, Logistic Regression, Naive Bayes, Multilayer Perceptron). 

In the second experiment, we perfomed a Mad-lib attack on the dataset, using a thesaurus that we built out of the dataset vocabulary scrapping the www.synonyms.com web pages, we modified each message of a held out subset (not used in the first experiment) with different rates of substitutions of original words with synonyms in order to evaluate the performance of the three representation models (BoW, TFIDF and BERT) in this kind of adversarial setting. 

We found that the classic models achieved a 94% Balanced Accuracy (BA) in the original dataset, whereas the BERT model obtained 96%. On the other hand, the Mad-lib adversarial experiment showed that BERT encodings manage to resist the attack, obtaining a similar BA performance of 96% with an average substitution rate of 1.82 words per message, and 95% with 3.34 words substituted per message. In contrast, the BA performance of the BoW and TFIDF encoders dropped to rates close to chance. Thus, these results provide evidence of the usefulness of BERT models to combat these type of ingenious spam attacks. 

**Authors:** Sergio A. Rojas 

**Emails:** srojas@udistrital.edu.co

*Universidad Distrital Francisco José de Caldas, Bogotá, Colombia*

---

## Repo contents

* .Tackling_spam_attacks_BERT.ipynb: A Jupyter NB that sets up the testbed, loads the data, configure the models, runs the experiments, and generates and saves the results reported in the paper
* ./data/spam/: this folder contains the dataset, the thesaurus, and files storing the results

--- END OF README ---



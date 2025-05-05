# Spam detection and evasion tool 

The main objective of this project is to classify spam emails and messages effeciently by coducting 3 main expirements (basic classifier, deep learning classifier and transformer based classifier) on 3 different evasion techniques (spacing, charswap, homoglyph) and comparing between them and introduce the best one (or hybrid method).
  
**Spam types**:
There are two main types of spam messages that we considered in this project:
- Normal spam messages (e.g. 'click the link for free money')
- Evasion spam emails/messages (e.g. 'cl   ick the link for fr33 monEy')

**Spam dataset**
This task was critical becasue this dataset will be shared among the three different models so it shouldn't be too much preprocessed (e.g.for example the words shouldn't be stemmed (playing shouldn't become play) because bert model will use it to understand context)
so 3 datasets were preprocessed which are:
1) Enron1
2) Enron2
3) SMS
each dataset is splitted to three main splits: train, val, test
so the models can use them directly, to ensure fair comparision
The datasets can be found here: 
this task was held by @Samiha


**Evasion types**:
There are many evasion methods that hackers use nowadays, for the purpose of this project and within the time frame, we managed to work on these 4 methods:
1) charswap
2) homoglyph
3) spacing
4) adversarial : Mixed leetspeak with dilution evasion techniques
each dataset is splitted to three main splits: train, val, test
so the models can use them directly, to ensure fair comparision

**Evasion dataset**:
in order to develop the classification model, we need evasion dataset
The evasion datasets was developed manually and it can be found here:
this task was held by @Tibor

**Main expirements**:
and in order to achieve this task, we conducted many methods:
- Basic classifiers: Logistic regression classifier and Naive Bayes classifier
- Deep learning classifier: Long Short Term memory model (LSTM)
- Transformer classifier : BERT
All of these 3 expirements share:
1) the same training, evaluation and test datasets (for fair comparision)
2) the same evaluation metrics (accuracy, precision, recall, f1-score)

**Basic classifiers**
This classifier is robust and powerful in many scenarios
you can find the results of using it here: 
[before_evasion](https://github.com/paulinaeb/IDaSec-project/blob/exp1/baseline-model.ipynb)
[after_evasion](https://github.com/paulinaeb/IDaSec-project/blob/exp1/baseline-model-evasion-version.ipynb)
this task was held by @Paulina

**Deep learning classifier**
This classifier is dynamic and can work with big datasets
you can find the results of using it here:
this task was held by @Samiha
[before_evasion](https://github.com/paulinaeb/IDaSec-project/blob/exp3/my_exp3/before_evasion.ipynb)
[after_evasion](https://github.com/paulinaeb/IDaSec-project/blob/exp3/my_exp3/after_evasion.ipynb)

**BERT classifier**
This classifier is one of the best models nowadays, it has some great applications
you can find the results of using it here:
this task was held by @Ahad
[before_evasion](https://github.com/paulinaeb/IDaSec-project/blob/exp2/LLM_BeforeEvasion.ipynb)
[after_evasion](https://github.com/paulinaeb/IDaSec-project/blob/exp2/LLM_After_Evasion.ipynb)







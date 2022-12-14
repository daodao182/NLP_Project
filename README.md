# The Simpsons
Predicting which character is speaking based on dialogue. 
This project is using NLP to train the training dataset ,and predicting the character part of the testing dataset

# Requirements
Python >=3.0<br />
Tensorflow >=2.0<br />
Numpy <br/>
GPU <br/>

# Pretraining
```read.csv``` :read dataset<br />
```dropna().reset_index(drop=True)```:remove missing values<br />
```token.lemma_```: remove stopwords<br />
```brief_cleaning```: remove non-alphabetic characters<br />
```preprocessing.LabelEncoder```:convert labels to vector<br />
```vocab_file``` : build a vocabulary file<br />
```do_lower_case```: lowercase all letters<br />
```tokenizer```: pass ```vocab_file``` and ```do_lower_case``` to the Tokenizer object

# Keras API

```
lay = tf.keras.layers.Dense(64, activation='relu')(clf_output)
    lay = tf.keras.layers.Dropout(0.2)(lay)
    lay = tf.keras.layers.Dense(32, activation='relu')(lay)
    lay = tf.keras.layers.Dropout(0.2)(lay)
    out = tf.keras.layers.Dense(5, activation='softmax')(lay)
```

# Training
Parameters: <br />
```validation_split```: improve the model performance after every epoch<br />
```epochs```: times of iteration <br />
```batch_size```: size of batch being trained<br />
```verbose```: how the output will be shown


# Running
This code needs to be run on a computer with GPU,or it will take very long time.<br />
The Notebook of Kaggle has GPU accelerator :GPU T4x2 and GPU P100, they are free for 30h per week


# References
https://www.kaggle.com/code/nayansakhiya/text-classification-using-bert/notebook</br>
https://www.kaggle.com/code/foolofatook/news-classification-using-bert</br>
https://www.kaggle.com/code/phongphamds/word2vec-using-gensim-library

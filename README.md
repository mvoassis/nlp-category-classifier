# **NLP - Text category classifier**

#### *Marcos V. O. Assis (mvoassis@gmail.com)*

***
> ## Objective: 

Generate an algorithm capable of classifying articles based on their titles.

> ## Language: 

For development and testing, words in Portuguese-BR were used.

> ## Approach:

1. Download Word2Vec pre-trained CBOW model from [NILC](http://nilc.icmc.usp.br/nilc/index.php/repositorio-de-word-embeddings-do-nilc) (cbow_s300)
2. Load the model using the Gensin library.
3. Vectorize the article's titles using the NLTK library and CBOW model.
4. Training a Logistic Regression classification model using the Scikit Learn library.

> ## Categories considered:

* Mundo (World)
* Cotidiano (Daily life)
* Mercado (Market)
* Esporte (Sports)
* Ilustrada (Illustrated)
* Colunas (Column)

> ## Files

* Train dataset -> [Link](https://caelum-online-public.s3.amazonaws.com/1638-word-embedding/treino.csv) - 90000 entries
* Test dataset  -> [Link](https://caelum-online-public.s3.amazonaws.com/1638-word-embedding/teste.csv) - 20513 entries

> ## Results

* 0.8 Accuracy score using CBOW (against 0.3 Accuracy from Dummy Classifier)
* Regarding individual categories, the proposed model achieved F1-Score:
  1. colunas - 0.78      
  2. cotidiano - 0.69
  3. esporte - 0.90
  4. ilustrada - 0.23
  5. mercado - 0.81
  6. mundo - 0.79
* CBOW is slightly better than Skipgram for this problem. 

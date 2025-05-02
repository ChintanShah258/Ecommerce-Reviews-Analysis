## 1. Project Overview  
This repository implements a complete NLP pipeline to clean, explore, model and visualize customer reviews from a women’s clothing e‑commerce dataset. We automatically label sentiment from ratings, train and compare multiple classifiers (Word2Vec+SVM, TF‑IDF+SVM, Naïve Bayes), extract key adjectives/verbs, generate word clouds, and perform topic modeling (LDA) for product categories. Finally, we slice insights by product ID, class name, and customer age groups, and produce interactive visualizations.

## 2. Key Features  

- **Data Ingestion & Cleaning**  
  - Load raw CSV, handle missing titles/reviews  
  - Normalize Unicode, remove punctuation, expand contractions  
  - Lowercase, remove stopwords, lemmatize  

- **Sentiment Labeling**  
  - Derive “human” sentiment from star ratings (Positive/Neutral/Negative)  
  - Compute TextBlob polarity, bucket into algorithmic sentiment labels  
  - Compare and report confusion matrix between rating‑based vs. TextBlob labels  

- **Feature Engineering & Classification**  
  - **Word2Vec**: train skip‑gram embeddings, average per document → Linear SVM & Multinomial NB  
  - **TF‑IDF**: vectorize corpus → Linear SVM & Multinomial NB  
  - Detailed classification reports & confusion matrices  

- **Lexical Analysis**  
  - Extract top 20 adjectives & verbs for each sentiment class (human vs. TextBlob)  
  - Generate comparative word clouds  

- **Exploratory Data Analysis**  
  - Count & mean polarity by Clothing_ID, Class_Name, Age_Groups  
  - Bar plots of top‑reviewed items and demographic segments  
  - Export Excel summary of age–class–item group stats  

- **Topic Modeling**  
  - Build 20‑topic LDA models for “Dresses” and “Knits”  
  - Print topic keywords; save interactive HTML via pyLDAvis  

- **Interactive Visualization**  
  - Holoviews bar charts for multi‑index DataFrames  
  - Panel dashboard scaffold for further extension  

## 3.Results & Insights

    Classification: ~80–85% accuracy predicting recommendation.

    Sentiment Alignment: ~75% agreement between rating‑based vs. TextBlob.

    Lexical Trends: Positive reviews: “comfortable,” “nice”; Negative: “tight,” “cheap.”

    Demographics: Age 25–30 shows highest positivity for Dresses.

    Topics: Themes: “fit/size,” “fabric quality,” “style/color.”

## 4.Next Steps

    Deploy interactive Panel dashboard

    Tune LDA hyperparameters (5–10 topics)

    Integrate BERT‑based sentiment classifiers

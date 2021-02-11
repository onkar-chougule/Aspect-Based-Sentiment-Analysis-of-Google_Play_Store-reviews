# Aspect-Based-Sentiment-Analysis-of-Google_Play_Store-reviews

* Scraping
  * Use [google_play_scraper package](https://pypi.org/project/google-play-scraper/) for scraping the Google play-store app reviews

* Cleaning
  * Convert emojis to corresponding text used [emoji package](https://pypi.org/project/emoji/) for greater inclusion
  * Remove punctuations
  * Remove stopwords
  
* Pre-processing
  * Convert to lower case
  * Perform stemming/ lemmatization depending upon data, I prefer lemmatization
  * Tokenize sentences into words
  
* Converting words into vectors
  * Use word2vec model from nlp to create word embeddings
  
* Sentiment Analysis based on aspects
  * Using word2vec find words having least distance from aspect words
  * Use [fuzzy-wuzzy](https://pypi.org/project/fuzzywuzzy/) to find all the reviews having words with embeddings similar to given aspect
  * Pass these reviews through sentiment analyser to get sentiment about given aspect
  * Use word cloud diagram for knowing the prominent aspect if they are not given to you
  * Use seaborn/matplotlib for visualization and comparision

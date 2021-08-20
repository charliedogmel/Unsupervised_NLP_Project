# Match My Music
## A Song Recommender System Matching Your Theme Song to More Theme Songs
Melissa Cooper

## Abstract

Music recommendation is a huge industry. Most people listen to music whose words or story they like or identify with. Wouldn't it be interesting if a system could recommend more similarly themed songs? Instead of considering genre, this would be a way to be introduced to new and different music whose subjects the user likes.


## Design

The NLP pipeline for this project involved many steps. First, I used spotipy and lyricsgenius APIs to acquire the data. Lyricsgenius is basically a python wrapper for http queries (web scraping) and it took four days to download all the lyrics. Next, preprocessing of all the lyrics was quite extensive due to a large amount of spam-like data in the lyrics. The cleaned data was run through various combinations of a vectorizer (CountVectorizer or TF-IDF) and then a topic modeler (NMF or LDA.) I also used TextBlob for sentiment analysis to explore how the crowdsourced sentiments of happy, sad, angry, and chill compared to the machine learning sentiments.

## Data

From the Spotify API, I found 1000 playlists in each emotion category (happy, sad, angry, chill) and pulled all the songs from those playlists yielding 2.2M songs. After some initial preprocessing for duplicates and missing data, lyricsgenius searched for each song's lyrics. This process took a very long time and in hindsight, the song list needed to be filtered even more. For instance, removing non-English song titles since the lyrics are most likely non-English.

Once the dataset was complete, EDA revealed a lot of garbage lyrics. This resulted in a highly specialized preprocessing step that reduced the dataset to 47k songs.

## Algorithms

*Preprocessing*

1. Song duplicates or same song listed with multiple release years
2. Emotion/mood multi-classification
3. Missing values
4. Remove non-English lyrics
5. Remove non-ASCII characters
6. Remove garbage from scraped lyrics: spam, transcripts, lists of songs, Congressional sessions,...
7. General lyrics cleaning: remove text in parenthesis like [Chorus] or (Person singing now)

*Topic Modeling*
  
Multiple combinations of vectorizers and topic modelers were implemented to discover the best combination. Starting from a baseline of CountVectorizer and NMF, then looped through the baseline adding more stop words, switching TF-IDF in for the vectorizer and using LDA instead of NMF.

Using CountVectorizer with LDA appeared to produce the best results for both topic modeling and the recommendation system. The topics were richer and a bit deeper, the recommender gave many insights.

*Recommendation/Sentiment/Visualization*
  
I used a basic cosine distance recommender and it performs fairly well. In the future it should incorporate the song's mood classification to provide more accurate recommendations.

I used TextBlob for sentiment analysis and it reflected the music and music moods accurately and provided more insight into the dataset.

Visualization is a huge part of NLP and provide viewpoints that topic word lists do not. Plotly and pyLDAvis were very useful in this respect.

## Tools

- Numpy and Pandas for data manipulation
- Scikit-learn CountVectorizer, TfidfVectorizer, NMF, LDA for modeling
- Plotly, pyLDAvis, Matplotlib, and Seaborn for plotting
- spotipy - python Spotify API
- lyricsgenius - python client for Genius.com API

## Communication

Presentation, slides, and write-up

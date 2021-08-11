# Unsupervised Learning & Natural Language Processing

# Question/need:

### What is the framing question of your analysis, or the purpose of the model/system you plan to build?

Using song lyrics, there are two possible framing questions:
- Create a recommendation system: Can the lyrics of a user requested song be used to recommend another song with a similar topic?
- Use supervised learning: Can a user requested emotion/mood classification of music be used to recommend a similarly classified song? Especially, will the topic modeling combined with musical features be effective in classifying songs into emotion categories?

### Who benefits from exploring this question or building this model/system?

The music industry is huge and the general public uses music recommender systems daily. In addition, businesses, restaurants, doctors' offices, lobbies, stores, and elevators use music to impart specific messages or moods to their customers so either system would be very useful to them.

# Data Description:

### What dataset(s) do you plan to use, and how will you obtain the data?

I will create the dataset using APIs. 

- Lyrics Genius: Use the python Lyrics Genius API, lyricsgenius, to obtain lyrics.
- Spotify: I can generate a database of songs and their metadata using the Spotify API for Python: spotipy. I can also search in Spotify for my emotion categories to find songs pre-labeled with the target for the supervised learning question.

### What is an individual sample/unit of analysis in this project? What characteristics/features do you expect to work with?

An individual unit of analysis is a song. I will work with lyrics and then their topic-modeled topics, and maybe the Spotify music features.

### If modeling, what will you predict as your target?

For the recommendation system, I will predict a related song. For the classification system, I will predict one of four emotions that describe each song in the test set.

# Tools:

### How do you intend to meet the tools requirement of the project?

I will use the python text processing libraries/tools (such as NLTK, spaCy, gensim, scikit-learn) for data handling. Other tools will include APIs, SQL, and visualization tools.

### Are you planning in advance to need or use additional tools beyond those required?

Maybe

# MVP Goal:

### What would a minimum viable product (MVP) look like for this project?

An MVP will include data aquisition, exploration, text preprocessing, and feature extraction.

# Mod-4-Project

## A Music Recommendation Model Using a Hybrid Approach
Music Recommendation Models use collaborative filtering and/or content based filtering to make predictions about user preferences.

Our hybrid model uses a combination of both filtering techniques. 

One of the major issues with music recommendations is the lack of explicit ratings for individual songs. Streaming services often have proprietary explicit rating data (e.g. Spotify thumbs up or thumbs down rating) but ultimately there is very little explicit ratings data on music, especially in publicly available data.

In order to get around this, our model uses Singular Value Decomposition, a form of matrix factorization, to estimate a user's rating for individual songs by use of listening history by comparing individual users' listening histories.

After determining the ratings, we built a neural network classifier for the individual user to find the patterns in the audio features for the songs that user's most enjoyed.

Ultimately this network can then be used to classify other audio, to find recommendations for the user.

### Data Sources
* [LastFM User Listening History Data](https://www.dtic.upf.edu/~ocelma/MusicRecommendationDataset/lastfm-1K.html)
* [Spotify API (for song features)](https://developer.spotify.com/documentation/web-api/reference/tracks/get-audio-features/)

### Tools Used
* [Surprise](http://surpriselib.com/) - Recommender System library built off Scikit-Learn
* [Keras](https://keras.io/), [Talos](https://github.com/autonomio/talos) - Neural Network (Keras) and Hyperparameter Tuning (Talos)
* Experiments done in [Amazon Sagemaker](https://aws.amazon.com/sagemaker/)

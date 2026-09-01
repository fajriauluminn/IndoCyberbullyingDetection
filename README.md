# Indonesian Twitter Cyberbullying Detection
A machine learning project for detecting and classifying cyberbullying in Indonesian social media text.

The project explores a hybrid **IndoBERTweet-BiGRU** architecture for text classification. IndoBERTweet is used to capture contextual representations of Indonesian social media text, while Bidirectional GRU (BiGRU) is used to capture sequential information from the resulting representations.

The project covers the complete machine learning pipeline, including data preparation, text preprocessing, automated labeling, model training, experimentation, and evaluation.

## Dataset

The dataset consists of Indonesian social media posts collected from Twitter/X using cyberbullying-related keywords.

The dataset contains text and metadata collected during the data collection process.

The main text-related features include:

| Feature | Description |
|---|---|
| `tweet_id` | Unique identifier of the tweet |
| `date` | Tweet publication date |
| `username` | Twitter/X username |
| `text` | Tweet text |
| `likes` | Number of likes |
| `retweets` | Number of retweets |
| `replies` | Number of replies |
| `keyword` | Keyword used during data collection |
| `lang` | Detected language |

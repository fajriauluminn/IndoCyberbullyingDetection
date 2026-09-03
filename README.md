# Indonesian Twitter Cyberbullying Detection
A machine learning project for detecting and classifying cyberbullying in Indonesian social media text.

## Project Background and Overview
The rapid growth of social media usage has increased the amount of user-generated content in Indonesian. Among this content, cyberbullying can appear in various forms, including abusive language, sexual harassment, hate speech, and body shaming.

Identifying cyberbullying manually is difficult and time-consuming, especially when dealing with large volumes of short and informal social media texts. Indonesian social media text also presents additional challenges due to slang, informal language, abbreviations, and contextual meaning.

Therefore, this project aims to develop a machine learning model that can automatically detect and classify cyberbullying in Indonesian social media text using a hybrid IndoBERTweet-BiGRU architecture. IndoBERTweet is used to capture contextual representations of Indonesian social media text, while Bidirectional GRU (BiGRU) is used to capture sequential information from the resulting representations.

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

## Exploratory Data Analysis

The EDA investigates:

- Dataset structure
- Missing values
- Duplicate records
- Text characteristics
- Label distribution
- Distribution of cyberbullying categories

## Data Preprocessing

Text preprocessing is performed to prepare Indonesian social media text for model training.

The preprocessing pipeline includes:

- Removing URLs
- Removing mentions
- Removing hashtags
- Removing emojis

## Automated Data Labeling

The dataset was automatically labeled using a zero-shot classification approach with **Gemini 2.5 Flash** and **Gemini 2.5 Flash-Lite**.

The two models independently classified each text into the predefined cyberbullying categories, only samples with matching labels from both models were retained for the final dataset.

A manually validated subset was also used to evaluate the agreement between the automated labeling process and human-validated labels.

### Label Distribution

The dataset contains five classification categories:

- Rude and Vulgar Words
- Sexual Harassment
- Hate Speech
- Body Shaming
- Non-Cyberbullying

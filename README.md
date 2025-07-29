 🧠 What I Did in the Code:

This project performs sentiment analysis on Twitter data using a structured pipeline of data processing and visualization. Here's a step-by-step breakdown:

 1. 📥 Loaded the Dataset
- Loaded the file `twitter_training.csv` which contains over 74,000 tweets with labeled sentiments.
- The original column names were non-standard, so I renamed them to `ID`, `Topic`, `Sentiment`, and `Text`.

 2. 🧹 Cleaned the Data
---> Dropped rows where the `Text` field was missing.
---> Created a new column `Cleaned_Text` by:
  - Lowercasing all words
  - Removing URLs, numbers, punctuation
  - Removing extra whitespace

 3. 📊 Visualized Sentiment Distribution:
---> Created a count plot showing how many tweets are Positive, Negative, or Neutral.
---> Updated Seaborn's syntax to avoid deprecation warnings (`hue=...`, `legend=False`).

 4. ☁️ Generated Word Clouds:
---> Created separate word clouds for each sentiment category.
---> Each word cloud shows the most common words in tweets of that sentiment.

 5. 🔠 Found Top 10 Words per Sentiment
---> Used `CountVectorizer` from scikit-learn to extract word frequencies.
---> Plotted horizontal bar charts showing the top 10 most frequent words in:
  - Positive tweets
  - Negative tweets
  - Neutral tweets
----> Applied updated `hue` and `palette` arguments to remove Seaborn future warnings.


 🧰 Technologies Used:

---> Python
---> Pandas & NumPy for data manipulation
---> Seaborn & Matplotlib for visualization
---> WordCloud for NLP visualization
---> CountVectorizer for text frequency analysis

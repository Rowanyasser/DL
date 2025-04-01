# DL
# Elissa Lyrics Preprocessing & Sentiment Analysis

## Project Overview
This project focuses on preprocessing Arabic song lyrics by Elissa, applying text cleaning, tokenization, stopword removal, stemming, and sentiment analysis. The goal is to prepare the lyrics dataset for natural language processing (NLP) tasks, such as emotion detection and further linguistic analysis.

## Features
- **Text Preprocessing**:
  - Cleaning special characters, diacritics, and unnecessary symbols.
  - Splitting non-space-separated stopwords to ensure accurate removal.
- **Tokenization**:
  - Splitting lyrics into individual words, ensuring each word is in a separate line.
- **Stopword Removal**:
  - Filtering out common Arabic stopwords after ensuring they are properly separated.
- **Stemming**:
  - Applying improved stemming techniques to retain meaning while reducing words to their root forms.
- **Sentiment Analysis**:
  - Classifying lyrics as positive, negative, or neutral using advanced models.

## File Structure
- `preprocessElissa.ipynb`: Jupyter Notebook containing the full preprocessing pipeline.
- `elissa_lyrics_preprocessed.csv`: CSV file with processed lyrics data.

## Installation
1. Clone the repository:
   ```bash
   git clone <repository_url>
   cd <repository_folder>
   ```
2. Install dependencies

## Usage
1. Open the Jupyter Notebook:
   ```bash
   jupyter notebook preprocessElissa.ipynb
   ```
2. Run all the cells to preprocess the lyrics dataset.
3. The final processed data will be saved as `elissa_lyrics_preprocessed.csv`.

## Sentiment Analysis Results
After applying sentiment analysis using the BERT-based model, the following results were obtained:

| Sentiment  | Count |
|------------|-------|
| **Positive**   | 30    |
| **Negative**   | 37    |
| **Neutral**    | 38    |

These results show a balanced distribution of sentiments across the lyrics dataset, with a slight lean toward negative sentiments.

## Potential Insights
- The prevalence of negative sentiments could suggest themes of longing, heartbreak, or emotional struggle in these songs, which is common in romantic or dramatic Arabic music.
- The positive songs might reflect themes of love, hope, or joy, as seen in titles like "مكتوبه ليك" or "هنغنى كمان وكمان".
- The neutral songs might indicate a more reflective or balanced emotional tone, neither overly joyful nor deeply sorrowful.

## Observations
1. **Sentiment Distribution**
   - Neutral sentiment is the most frequent (~36%), followed by negative (~35%), and then positive (~29%).
   - This suggests a balance between emotionally intense (negative/positive) and reflective (neutral) lyrics.

2. **Sentiment Trends Over the Years**
   - Negative sentiment **peaks in 2016 and 2018**, aligning with themes of heartbreak or emotional struggle.
   - Positive sentiment **becomes more common in 2018 and 2020**, indicating a potential shift toward uplifting themes.
   - Neutral sentiment **remains dominant in 2016 and 2018**, reflecting a contemplative tone during those years.

3. **Influence of Lyricists and Composers**
   - Certain lyricists (e.g., **Ahmed El Gendy**) lean toward negative themes.
   - Some composers (e.g., **Osama Rahbani**) also contribute to more negative sentiment.
   - Others, like **Ahmed Marzouk**, create a mix of neutral and positive tones.

## Future Improvements
- Further fine-tuning of Arabic stemming for better accuracy.
- Experimenting with different sentiment analysis models for improved classification.
- Enhancing emotion detection by expanding categories and using deep learning techniques.


# DL
# Elissa Lyrics Preprocessing & Sentiment + Emotion Analysis

## Project Overview
This project focuses on preprocessing Arabic song lyrics by the Lebanese artist Elissa. It includes a detailed pipeline for data cleaning, tokenization, stopword removal, stemming, and both sentiment and emotion classification. It aims to enable NLP tasks such as emotional profiling and linguistic insights from Arabic music. The notebook also includes visualizations for sentiment analysis and emotional detection.

## Features
- **Text Preprocessing**:
  - Cleaning special characters, diacritics, and unnecessary symbols.
  - Splitting non-space-separated stopwords to ensure accurate removal.
- **Tokenization & Stopword Removal**:
  - Proper handling of attached Arabic stopwords and word segmentation.
  - Ensures clean and meaningful word tokens for analysis.
- **Stemming**:
  - Uses improved stemmers adapted to Arabic morphology, enhancing root extraction accuracy.
- **Sentiment Analysis**:
  - Sentiment labels (Positive, Negative, Neutral) were generated using a BERT-based Arabic sentiment model.
- **Emotion Detection**:
  - Emotions extracted using lexicon-based and ML models into classes like joy, sadness, anger, fear, surprise, and neutral.
- **Top TF-IDF Words**:
  - Key discriminative words were identified using TF-IDF ranking, per song.

## File Structure
- `preprocessElissa.ipynb`: Jupyter Notebook containing the full preprocessing pipeline.
- `elissa_lyrics_preprocessed.csv`: CSV file with processed lyrics data with sentiment analysis.
- `elissa_lyrics_preprocessed_with_emotion_tfidf.csv`: Preprocessed lyrics with sentiment analysis, emotion detection, and top TF-IDF words.

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

## Potential Insights for sentiment analysis
- The prevalence of negative sentiments could suggest themes of longing, heartbreak, or emotional struggle in these songs, which is common in romantic or dramatic Arabic music.
- The positive songs might reflect themes of love, hope, or joy, as seen in titles like "مكتوبه ليك" or "هنغنى كمان وكمان".
- The neutral songs might indicate a more reflective or balanced emotional tone, neither overly joyful nor deeply sorrowful.

## Emotion Distribution
After applying emotional detection, the following results were obtained:

| Emotion  | Count |
|------------|-------|
| **Sadness**   | 32    |
| **Joy**   | 18    |
| **Neutral**    | 24    |
| **Fear**   | 13    |
| **Surprise**   | 10    |
| **Anger**    | 8    |

- Sadness is the dominant emotion, reflecting themes of heartbreak or deep emotional reflection.
- Joy and surprise reflect the celebratory or hopeful tones in some songs.
- Anger and fear appear less frequently, often in songs of confrontation or longing.

## Potential Insights for emotional detection
- Arabic lyrics by Elissa follow traditional themes of romance, sorrow, and emotional healing.
- Lyrics reflect introspective and relationship-driven storytelling.
- Emotional profiling suggests a resonance with heartbreak and personal struggle, interspersed with moments of hope.


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

4. **Sentiment & Emotion Breakdown**
   - Sad songs often labeled with both negative sentiment and sadness/fear emotions.
   - Positive songs tend to express joy, and are more common post-2015.

## Top TF-IDF Word Insights
- "انا","قلبى","حبيبى","عيش","دموع" are among the most prominent across the lyrics.
- Indicates a focus on personal pronouns, emotions, and interpersonal themes.
- In the visuals in the notebook we could see that the word "انا" is the top across all songs which indicates that she might be egoistic and completely self-absorbed.
  
## Future Improvements
- Further Fine-tune Arabic stemmers or use character-level models.
- Incorporate transformer-based Arabic emotion classifiers for more nuanced detection.
-  Expand analysis to include metaphors, figurative language, and theme clustering.


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

## Future Improvements
- Further fine-tuning of Arabic stemming for better accuracy.
- Experimenting with different sentiment analysis models for improved classification.
- Enhancing emotion detection by expanding categories and using deep learning techniques.



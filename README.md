# DL
# Elissa Lyrics Preprocessing & Sentiment + Emotion Analysis

## Project Overview
This project focuses on preprocessing Arabic song lyrics by the Lebanese artist Elissa. It includes a detailed pipeline for data cleaning, tokenization, stopword removal, stemming, and both sentiment and emotion classification. It aims to enable NLP tasks such as emotional profiling and linguistic insights from Arabic music. The notebook also includes visualizations for sentiment analysis, emotional detection, and TF-IDF keyword analysis by year, lyricist, and composer.

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
  - Emotions extracted using lexicon-based and ML models into classes like joy, sadness, anger, fear, surprise, disgust, and neutral.
- **Top TF-IDF Words**:
  - Key discriminative words were identified using TF-IDF ranking, per song and by year.

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

### Sentiment Distribution by Lyricist
The sentiment distribution for selected lyricists highlights variations in emotional tone:

| Lyricist         | Positive | Neutral | Negative |
|------------------|----------|---------|----------|
| احمد الجندى      | 0.000    | 0.200   | 0.800    |
| احمد مرزوق      | 0.333    | 0.667   | 0.000    |
| اسامه مصطفى     | 0.333    | 0.000   | 0.667    |
| الياس ناصر      | 0.833    | 0.167   | 0.000    |
| امير طعيمة      | 0.000    | 0.750   | 0.250    |
| نادر عبدالله    | 0.421    | 0.263   | 0.316    |

- **Observations**:
  - احمد الجندى's lyrics are predominantly negative (80%), suggesting themes of sorrow or struggle.
  - الياس ناصر leans heavily toward positive sentiments (83.3%), indicating uplifting or joyful themes.
  - نادر عبدالله shows a balanced distribution, with a slight preference for positive sentiments (42.1%).

### Sentiment Distribution by Composer
The sentiment distribution for selected composers reveals their influence on emotional tone:

| Composer        | Positive | Neutral | Negative |
|-----------------|----------|---------|----------|
| تامر عاشور     | 0.667    | 0.000   | 0.333    |
| تامر على       | 0.333    | 0.333   | 0.333    |
| رامى جمال      | 0.000    | 0.500   | 0.500    |
| محمد رحيم      | 0.300    | 0.300   | 0.400    |
| محمد يحيى      | 0.286    | 0.429   | 0.286    |
| وليد سعد       | 0.143    | 0.714   | 0.143    |

- **Observations**:
  - تامر عاشور's compositions are mostly positive (66.7%), reflecting hopeful or romantic themes.
  - وليد سعد favors neutral sentiments (71.4%), suggesting a reflective or balanced tone.
  - محمد رحيم has a slight tilt toward negative sentiments (40%), indicating emotional depth.

### Statistical Analysis of Sentiment
- **Kruskal-Wallis Test for Lyricists**: Statistic=14.60, p-value=0.1474
  - No significant difference in sentiment across lyricists (p >= 0.05).
- **Kruskal-Wallis Test for Composers**: Statistic=5.38, p-value=0.7998
  - No significant difference in sentiment across composers (p >= 0.05).
- **Spearman Correlation for Sentiment Score vs. Year**: Correlation=-0.38, p-value=0.1816
  - No significant trend in sentiment over time (p >= 0.05).
 - **The lack of significant differences suggests that sentiment in Elissa's songs may be driven by factors other than the lyricist or composer like:**
  - Elissa's artistic style or preferences.
  - The dataset's size or distribution.
  - The sentiment analysis model's limitations.

## Emotion Distribution
After applying emotional detection, the following results were obtained:

| Emotion  | Count |
|----------|-------|
| **Sadness**   | 32    |
| **Joy**       | 18    |
| **Neutral**   | 24    |
| **Fear**      | 13    |
| **Surprise**  | 10    |
| **Anger**     | 8     |

- Sadness is the dominant emotion, reflecting themes of heartbreak or deep emotional reflection.
- Joy and surprise reflect the celebratory or hopeful tones in some songs.
- Anger and fear appear less frequently, often in songs of confrontation or longing.

### Emotion Distribution by Lyricist
The emotion distribution for selected lyricists provides deeper insights:

| Lyricist         | Anger | Disgust | Fear | Joy  | Neutral | Sadness |
|------------------|-------|---------|------|------|---------|---------|
| احمد الجندى      | 0.000 | 0.000   | 0.000| 0.200| 0.000   | 0.800   |
| احمد مرزوق      | 0.000 | 0.000   | 0.000| 0.333| 0.333   | 0.333   |
| اسامه مصطفى     | 0.000 | 0.000   | 0.333| 0.333| 0.000   | 0.333   |
| الياس ناصر      | 0.167 | 0.000   | 0.000| 0.000| 0.333   | 0.500   |
| امير طعيمة      | 0.000 | 0.000   | 0.250| 0.250| 0.000   | 0.500   |
| نادر عبدالله    | 0.158 | 0.000   | 0.105| 0.211| 0.211   | 0.316   |

- **Observations**:
  - احمد الجندى's lyrics are heavily sadness-driven (80%), aligning with negative sentiment.
  - الياس ناصر shows a mix of sadness (50%) and neutral (33.3%), with some anger (16.7%).
  - نادر عبدالله has a balanced emotional profile, with sadness (31.6%) and joy (21.1%) prominent.

### Emotion Distribution by Composer
The emotion distribution for selected composers highlights their emotional contributions:

| Composer        | Anger | Disgust | Fear | Joy  | Neutral | Sadness |
|-----------------|-------|---------|------|------|---------|---------|
| تامر عاشور     | 0.000 | 0.000   | 0.000| 0.000| 0.333   | 0.333   |
| تامر على       | 0.000 | 0.000   | 0.000| 0.333| 0.333   | 0.333   |
| رامى جمال      | 0.000 | 0.000   | 0.000| 0.250| 0.500   | 0.250   |
| محمد رحيم      | 0.100 | 0.100   | 0.000| 0.300| 0.000   | 0.500   |
| محمد يحيى      | 0.071 | 0.000   | 0.286| 0.071| 0.143   | 0.357   |
| وليد سعد       | 0.143 | 0.000   | 0.143| 0.286| 0.286   | 0.143   |

- **Observations**:
  - محمد رحيم's compositions are sadness-heavy (50%), with some joy (30%) and anger (10%).
  - وليد سعد shows a balanced emotional distribution, with equal contributions from sadness, joy, and neutral (14.3% each).
  - محمد يحيى has a notable fear component (28.6%) alongside sadness (35.7%).


### Emotion Distribution by Year
The emotion distribution over time reveals evolving emotional themes:

| Year | Anger | Disgust | Fear | Joy  | Neutral | Sadness | Surprise |
|------|-------|---------|------|------|---------|---------|----------|
| 2000 | 0.000 | 0.000   | 0.000| 0.000| 0.400   | 0.600   | 0.000    |
| 2002 | 0.200 | 0.000   | 0.200| 0.200| 0.200   | 0.200   | 0.000    |
| 2004 | 0.000 | 0.000   | 0.000| 0.000| 0.000   | 1.000   | 0.000    |
| 2006 | 0.000 | 0.000   | 0.167| 0.000| 0.167   | 0.500   | 0.167    |
| 2012 | 0.000 | 0.000   | 0.000| 0.222| 0.222   | 0.556   | 0.000    |
| 2016 | 0.000 | 0.000   | 0.133| 0.333| 0.067   | 0.400   | 0.067    |
| 2018 | 0.067 | 0.000   | 0.133| 0.133| 0.133   | 0.467   | 0.067    |
| 2022 | 0.000 | 0.000   | 0.000| 0.750| 0.000   | 0.250   | 0.000    |

- **Observations**:
  - 2004 is dominated by sadness (100%), reflecting intense emotional themes.
  - 2022 shows a strong shift toward joy (75%), indicating more uplifting themes.
  - 2018 has a balanced mix, with sadness (46.7%) and smaller contributions from fear, joy, and neutral (13.3% each).

## Potential Insights for Sentiment Analysis
- The prevalence of negative sentiments could suggest themes of longing, heartbreak, or emotional struggle in these songs, which is common in romantic or dramatic Arabic music.
- The positive songs might reflect themes of love, hope, or joy, as seen in titles like "مكتوبه ليك" or "هنغنى كمان وكمان".
- The neutral songs might indicate a more reflective or balanced emotional tone, neither overly joyful nor deeply sorrowful.
- Lyricists like احمد الجندى contribute to negative themes, while الياس ناصر leans toward positivity.
- Composers like تامر عاشور add positive tones, while محمد رحيم often evokes negative sentiments.

## Potential Insights for Emotional Detection
- Arabic lyrics by Elissa follow traditional themes of romance, sorrow, and emotional healing.
- Lyrics reflect introspective and relationship-driven storytelling.
- Emotional profiling suggests a resonance with heartbreak and personal struggle, interspersed with moments of hope.
- Sadness dominates across lyricists, composers, and years, but joy becomes more prominent in later years (e.g., 2022).
- Fear and anger are less frequent but appear in specific contexts, such as محمد يحيى's compositions or earlier years like 2002.

## Observations
1. **Sentiment Distribution**
   - Neutral sentiment is the most frequent (~36%), followed by negative (~35%), and then positive (~29%).
   - This suggests a balance between emotionally intense (negative/positive) and reflective (neutral) lyrics.

2. **Sentiment Trends Over the Years**
   - Negative sentiment peaks in 2016 and 2018, driven by high sadness percentages (40% and 46.7%, respectively), reflecting themes of heartbreak and emotional turmoil in these years.
   - Positive sentiment is most prominent in 2016 (33.3% joy) and 2022 (75% joy), signaling a shift toward uplifting and hopeful themes, particularly in later years.
   - Neutral sentiment remains consistent but not dominant across years, with notable presence in 2000 (40%) and 2012 (22.2%), suggesting reflective or balanced tones in specific periods.

3. **Influence of Lyricists and Composers**
   - Certain lyricists (e.g., **احمد الجندى**) lean toward negative themes.
   - Some composers (e.g., **محمد رحيم**) also contribute to more negative sentiment.
   - Others, like **الياس ناصر** (lyricist) and **تامر عاشور** (composer), create more positive tones.

4. **Sentiment & Emotion Breakdown**
   - Sad songs often labeled with both negative sentiment and sadness/fear emotions.
   - Positive songs tend to express joy and are more common post-2015.
   - Emotional shifts are evident, with joy increasing in 2022 and sadness dominating earlier years like 2004.


## Top TF-IDF Word Insights
- "انا", "قلبى", "حبيبى", "عيش", "دموع" are among the most prominent across the lyrics.
- Indicates a focus on personal pronouns, emotions, and interpersonal themes.
- In the visuals in the notebook, we could see that the word "انا" is the top across all songs, which indicates that she might be egoistic and completely self-absorbed.

### Top TF-IDF Keywords by Year
| Year | Keywords |
|------|----------|
| 2016 | حبيبى, قلب, حضن, بقى, قلبى |
| 2018 | حشتونى, قلبى, دى, لسه, كرهنى |
| 2014 | حب, تنى, قبل, عرف, قلبى |
| 2012 | عين, اقل, ايد, فيك, حبيبى |
| 2020 | نست, صحب, اله, كنت, وحد |
| 2006 | حكي, كنت, منى, حكايتى, معك |
| 2000 | وين, بدى, قلبى, عرف, يلى |
| 2002 | قلبى, يلى, قول, شو, عاك |
| 2009 | بلی, ليه, حبیبی, عرفش, كسر |
| 2022 | يما, ضمير, دقق, يسم, زهر |
| 2023 | شى, ندم, درب, عقد, لحب |
| 2004 | اعش, خلينى, بعد, رجع, سوا |
| 2007 | يلى, يبا, علا, بلك, خد |
| 2010 | دمع, ملی, علی, سمع, روح |

- **Insights**:
  - 2016 and 2014 focus on romantic and emotional themes (e.g., "حبيبى", "قلبى").
  - 2018 includes longing and conflict (e.g., "حشتونى", "كرهنى").
  - 2022 and 2023 introduce unique themes like conscience ("ضمير") and regret ("ندم").

## Future Improvements
- Further fine-tune Arabic stemmers or use character-level models.
- Incorporate transformer-based Arabic emotion classifiers for more nuanced detection.
- Expand analysis to include metaphors, figurative language, and theme clustering.
- Explore deeper statistical correlations between lyricists, composers, and emotional themes.
- Analyze the impact of specific albums or song genres on sentiment and emotion.

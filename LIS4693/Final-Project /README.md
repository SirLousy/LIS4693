# Anime Trends and Type Prediction Using Text Mining

## Project Overview

This final project analyzes anime synopsis text using text mining and machine learning. The goal was to explore patterns in anime descriptions and predict the anime type, such as TV, Movie, OVA, ONA, Special, or Music.

The project uses text preprocessing, sentiment analysis, topic modeling, and supervised machine learning to better understand how anime synopsis text connects to anime format and audience trends.

## Dataset

The dataset used for this project is the TidyTuesday Anime dataset from April 23, 2019.

Dataset link:  
https://raw.githubusercontent.com/rfordatascience/tidytuesday/main/data/2019/2019-04-23/tidy_anime.csv

The dataset includes anime titles, synopsis text, type, genre, studio, ratings, popularity, members, and other anime related information. For this project, the synopsis column was used as the main text field, and the type column was used as the label for prediction.

## Contents

- `FP.ipynb`  
  Main Google Colab notebook with the full project analysis, including data loading, preprocessing, text mining, machine learning, evaluation, and visualizations.

- `data/tidy_anime.csv`  
  Dataset used for the project.

- `figures/sentiment_distribution.png`  
  Visualization showing the distribution of sentiment scores across anime synopses.

- `figures/confusion_matrix.png`  
  Confusion matrix for the best machine learning model.

- `poster/anime_trends_final_poster.pdf`  
  Final poster file for the project.

## Text Preprocessing

The synopsis text was cleaned before analysis. The preprocessing steps included lowercasing text, removing punctuation and numbers, removing extra spaces, and creating a cleaned synopsis column.

Text was then converted into numerical features using TF-IDF and CountVectorizer so it could be used for topic modeling and machine learning.

## Text Mining Methods

### Sentiment Analysis

VADER sentiment analysis was used to measure the emotional tone of anime synopses. This method was chosen because it is lexicon based, easy to interpret, and works well on short to medium text.

### Topic Modeling

Latent Dirichlet Allocation, also known as LDA, was used to discover common themes in the anime synopsis text. The topic modeling results showed repeated themes such as action, battles, romance, school life, fantasy, magic, adventure, science fiction, and future technology.

## Machine Learning

The project tested machine learning models to predict anime type from synopsis text. Logistic Regression was selected as the best performing model because it had the strongest overall performance and balanced precision and recall across the anime type categories.

The prediction labels included:

- TV
- Movie
- OVA
- ONA
- Special
- Music

## Key Results

The Logistic Regression model achieved an accuracy of about 64 percent. The model performed better on anime types with stronger text patterns and more examples in the dataset. Some anime types were harder to classify because their synopsis descriptions overlap with other types.

The sentiment analysis showed that anime synopses have a wide range of emotional tones, with many descriptions falling near neutral, slightly positive, or slightly negative.

The topic modeling results showed that anime descriptions often repeat major themes related to action, fantasy, romance, school, adventure, and science fiction.

## Main Insights

Anime synopsis text can be useful for identifying broad trends in anime type and themes. Text mining helped reveal emotional and thematic patterns in the dataset, while machine learning showed that anime type can be predicted from synopsis text with moderate accuracy.

## Limitations

Some anime types are difficult to separate because their synopsis text can be very similar. For example, TV anime, OVAs, and Specials may share similar language if they belong to the same franchise or genre. The model also depends on the quality and length of the synopsis text.

## How to Run

1. Open `FP.ipynb` in Google Colab.
2. Run the notebook from top to bottom.
3. The notebook loads the dataset, cleans the text, performs text mining, trains the machine learning model, and generates results.
4. Output figures and result files are included in the `figures` and `results` folders.

## Tools and Libraries

- Python
- Pandas
- NumPy
- NLTK
- VADER Sentiment Analysis
- Scikit-learn
- Plotly
- Matplotlib

## Project Links

Dataset:  
https://raw.githubusercontent.com/rfordatascience/tidytuesday/main/data/2019/2019-04-23/tidy_anime.csv

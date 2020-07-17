# Predicting Song Popularity

Through linear regression modeling, this project aims to predict the popularity of a song. 

## The Dataset 

The final dataset used in this project was a compilation of a 2,000 song Spotify dataset sourced from Kaggle along with additional data gathered from API requests to Spotify's API via Spotipy.   

The **target variable** assessed was a popularity score for each song. 
- From Spotify's documentation - the popularity score is a calculation of number of plays and how recent those plays were.
- I wanted to see if song and artist elements could predict the popularity score. 

The **explantory variables** covered a range of characteristics on each song, from specific audio features like BPM, valence and duration, to more categorical data such as, genre, year released and artist follower count. 

## EDA 

**Target Distribution:** 

<img src="/images/targetdist.png" width="550">

**Correlation heatmap:** 

<img src="/images/correlationheat.png" width="1000">

**Numerical Feature Distribution:** 

<img src="/images/featdist.png" width="1000">


## Feature Engineering - Polynomial Transformation

After my EDA and running a baseline linear regression model, I applied polynomial transformation to the 2nd degree to all of my song audio features. This created interactions among the different song elements, which in hindsight really made sense because it’s the combination of elements that make up a song. A song is never just one audio feature.

## Conclusion

My final model wasn’t as predictive as I had hoped, explaining only 28% (R-squared) of the amount of variation in song popularity. However, after analyzing my coefficients, there were a few takeaways to be noted. The following features had the most positive and negative impact on popularity.

Most positive:
- Number of years since release
- Artist follower count
- Danceability

Most negative:
- Indie Genre
- Acousticness & Speechiness

## Contents of this project repository:

  1. Data Folder: all csvs stored here and pkled data post cleaning 
  2. Notebooks Folder: all work in progress notebooks - cleaning, EDA, Modeling
  3. Final.ipynb - final project notebook
  4. Presentation - copy of final presentation deck


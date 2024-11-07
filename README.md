# ECE2112-Exploratory-Data-Analysis-on-Spotify-2023-Dataset

## Overview of Guide Questions
In this repository, you will find my code for the Exploratory Data Analysis on Spotify 2023 Dataset. The code is divided into seven parts for a more in-depth analysis, namely:

### I. Overview of Dataset
**1. How many rows and columns does the dataset contain?**
  - The .csv dataset was loaded into the Jupyter Notebook and converted into a dataframe using the pandas functions *pd.read_csv* and *pd.DataFrame*. 

**2. What are the data types of each column? Are there any missing values?**
  - The data types were displayed alongside their respective columns in a new dataframe using the pandas functions *.dtypes* and *pd.DataFrame*.
    
### II. Basic Descriptive Statistics
**1. What are the mean, median, and standard deviation of the streams column?**
  - The mean, median, and standard deviation of the values in the *'streams'* column were acquired using the pandas functions *.mean()*, *.median()*, and *.std()*.

**2. What is the distribution of released_year and artist_count? Are there any noticeable trends or outliers?**
  - The distribution of released_year and the distribution of artist_count were displayed using the countplot feature in the seaborn library, which can be executed using *sns.countplot*.

### III. Top Performers
**1. Which track has the highest number of streams? Display the top 5 most streamed tracks.**
  - The top five most streamed tracks were counted using the pandas functions *.sort_values()* and *.head()* in descending order.
    
**2. Who are the top 5 most frequent artists based on the number of tracks in the dataset?**
  - The top five most frequent artists based on the number of streams were counted using the pandas functions *.value_counts()* and *.head()*. The series was converted into a dataframe by resetting the index using *.reset_index()*.
    
### IV. Temporal Trends
**1. Analyze the trends in the number of tracks released over time. Plot the number of tracks released per year.**
  - The top five years with the most released tracks were counted using the pandas function *.value_counts()* and *.head()*. The series was converted into a dataframe by resetting the index using *.reset_index()*. The number of tracks released for all years included in the dataset were displayed in a line graph using the line plot feature in the seaborn library, which can be used through *sns.lineplot*.
    
**2. Does the number of tracks released per month follow any noticeable patterns? Which month sees the most releases?**
  - Likewise, the top five months with the most released tracks were counted using the pandas function *.value_counts()* and *.head()*. The series was converted into a dataframe by resetting the index using *.reset_index()*. The number of tracks released for all months included in the dataset were displayed in a line graph using the line plot feature in the seaborn library, which can be executed using *sns.lineplot*.
    
### V. Genre and Music Characteristics
**1. Examine the correlation between streams and musical attributes like bpm, danceability_%, and energy_%. Which attributes seem to influence streams the most?**
  - The patterns were graphed using the seaborn function *sns.lineplot* with streams being plotted against the musical attributes bpm, danceability_%, and energy_% in the first, second, and third plots, respectively.

**2. Is there a correlation between danceability_% and energy_%? How about valence_% and acousticness_%?**
  - Similarly, the trends were graphed using the seaborn function *sns.lineplot*. The musical attributes danceability_% and energy_% were grouped together, as well as valence_% and acousticness_%.

### VI. Platform Popularity
**1. How do the numbers of tracks in spotify_playlists, spotify_charts, and apple_playlists compare? Which platform seems to favor the most popular tracks?**
  - In order to sum the number of tracks using the pandas function *.value_counts()* and *.sum()*, the non-numeric numbers in the columns 'in_spotify_playlists', 'in_spotify_charts', and 'in_apple_playlists' were converted using *pd.to_numeric, errors = coerce*. The resulting data was displayed in a bar plot executed using the matplotlib feature *plt.bar*.

### VII. Advanced Analysis
**1. Based on the streams data, can you identify any patterns among tracks with the same key or mode (Major vs. Minor)?**
  - The key and streams columns were grouped together using the *.groupby* feature to show them side-by-side in a dataframe. The total streams for each key were acquired using *.sum()* and the dataframe was organized using *.sort_index()* and *.reset_index()*. Likewise, the same code pattern was used for the mode. These trends in these dataframes were displayed using the matplotlib feature *plt.bar*.

**2. Do certain genres or artists consistently appear in more playlists or charts? Perform an analysis to compare the most frequently appearing artists in playlists or charts.**

**Note: a summary of answers to these questions can be found at the end of my code inside the Jupyter Notebook.**

## Getting Started
### File Inclusions
1. **Exploratory Data Analysis on Spotify 2023 Dataset - Dayao.ipynb** - Jupyter Notebook containing code for Exploratory Data Analysis on Spotify 2023 Dataset
2. **spotify-2023.csv** - given Spotify 2023 data

### Dependencies
The following software and libraries were used in the completion of this experiment:
- Anaconda Navigator 2.6.0<br>
- Jupyter Notebook 7.0.8
- pandas (Python Data Analysis) library
- matplotlib library
- seaborn library

## Authors
Sophia Nicole C. Dayao
<br>
2ECE-C

## Version History
**Version 1.0 - November 7, 2024**
- created *README* file
- uploaded *spotify-2023.csv* dataset

# ECE2112-Exploratory-Data-Analysis-on-Spotify-2023-Dataset

## Description
In this repository, you will find my code for the Exploratory Data Analysis on Spotify 2023 Dataset. The code is divided into seven parts for a more in-depth analysis, namely Overview of Dataset, Basic Descriptive Statistics, Top Performers, Temporal Trends, Genre and Music Characteristics, Platform Popularity, and Advanced Analysis.

## Getting Started
### File Inclusions
1. **Exploratory Data Analysis on Spotify 2023 Dataset - Dayao.ipynb** - Jupyter Notebook containing code for Exploratory Data Analysis on Spotify 2023 Dataset
2. **spotify-2023.csv** - given Spotify 2023 data

### Dependencies
The following software and libraries were used in the completion of this experiment:
- Anaconda Navigator 2.6.0<br>
- Jupyter Notebook 7.0.8
- Pandas (Python Data Analysis) library
- Matplotlib library
- Seaborn library

## Guide Questions
### I. Overview of Dataset
**1. How many rows and columns does the dataset contain?**
  - The .csv dataset was loaded into the Jupyter Notebook and converted into a dataframe using the pandas functions *pd.read_csv* and *pd.DataFrame*.
  
  - **Answer**: The dataset contains 953 rows and 24 columns.

**2. What are the data types of each column? Are there any missing values?**
  - The data types were displayed alongside their respective columns in a new dataframe using the pandas functions *.dtypes* and *pd.DataFrame*.
  
  - **Answer**: The columns of the dataset are composed of only two data types, which are 'integer’ and 'object'.
      
### II. Basic Descriptive Statistics
**1. What are the mean, median, and standard deviation of the streams column?**
  - The mean, median, and standard deviation of the values in the *'streams'* column were acquired using the pandas functions *.mean()*, *.median()*, and *.std()*.

- **Answer**: The mean of the streams column is 514.1 million, its median is 290.5 million, and its standard deviation is 566.9 million.
  
**2. What is the distribution of released_year and artist_count? Are there any noticeable trends or outliers?**
  - The distribution of released_year and the distribution of artist_count were displayed using the countplot feature in the seaborn library, which can be executed using *sns.countplot*.

- **Answer**: The first graph shows a significant increase in track releases in the 2010s, with a sharp spike from 2021 to 2023, especially in 2022. During the COVID-19 pandemic, artists turned to digital releases since there were tight restrictions on live performances. With easy access to home recording tools and a high demand for new music, many musicians released more tracks during this time to connect with their audiences.

  Meanwhile, the second graph shows that most tracks feature a single artist, while the number of tracks decreases as the number of artists involved increases. This suggests that there is a trend toward solo releases or small collaborations, while multi-artist tracks are outliers.
  
### III. Top Performers
**1. Which track has the highest number of streams? Display the top 5 most streamed tracks.**
  - The top five most streamed tracks were counted using the pandas functions *.sort_values()* and *.head()* in descending order.

- **Answer**: The top 5 most streamed tracks are Blinding Lights	with 3.7 billion streams; Shape of You	with 3.6 billion streams; Someone You Loved with 2.89 billion streams; Dance Monkey with 2.86 billion streams; and Sunflower - Spider-Man: Into the Spider-Verse with 2.8 billion streams.

**2. Who are the top 5 most frequent artists based on the number of tracks in the dataset?**
  - The top five most frequent artists based on the number of streams were counted using the pandas functions *.value_counts()* and *.head()*. The series was converted into a dataframe by resetting the index using *.reset_index()*.

- **Answer**: The top 5 most frequent artists are Taylor Swift with 34 tracks, The Weeknd with 22 tracks, Bad Bunny and SZA with 19 tracks each, and Harry Styles with 17 tracks.
   
### IV. Temporal Trends
**1. Analyze the trends in the number of tracks released over time. Plot the number of tracks released per year.**
  - The top five years with the most released tracks were counted using the pandas function *.value_counts()* and *.head()*. The series was converted into a dataframe by resetting the index using *.reset_index()*. The number of tracks released for all years included in the dataset were displayed in a line graph using the line plot feature in the seaborn library, which can be used through *sns.lineplot*.

- **Answer**: The line graph begins to rise somewhere between the years 2000 and 2020, suggesting that there is an increase in the number of released tracks during the 2010s. It can be seen that there is a noticeable spike after the year 2020, particularly in 2022, with 402 released tracks.
  
**2. Does the number of tracks released per month follow any noticeable patterns? Which month sees the most releases?**
  - Likewise, the top five months with the most released tracks were counted using the pandas function *.value_counts()* and *.head()*. The series was converted into a dataframe by resetting the index using *.reset_index()*. The number of tracks released for all months included in the dataset were displayed in a line graph using the line plot feature in the seaborn library, which can be executed using *sns.lineplot*.

- **Answer**: The line graph indicates that the number of tracks released varies per month. Months like January (134 tracks) and May (128 tracks) have the highest number of tracks released, while August (64 tracks) has the lowest number of released tracks. While the fluctuations are clearly captured by the line graph, there does not appear to be any consistent trend over the span of one year.
  
### V. Genre and Music Characteristics
**1. Examine the correlation between streams and musical attributes like bpm, danceability_%, and energy_%. Which attributes seem to influence streams the most?**
  - The patterns were graphed using the seaborn function *sns.lineplot* with streams being plotted against the musical attributes bpm, danceability_%, and energy_% in the first, second, and third plots, respectively.

- **Answer**: The line graphs show that none of these attributes show a clear or strong correlation with streams. There are some significant peaks in each graph, but they do not follow a predictable pattern for any specific attribute. This suggests that streams are not significantly influenced by bpm, danceability_%, and energy_%.
  
**2. Is there a correlation between danceability_% and energy_%? How about valence_% and acousticness_%?**
  - Similarly, the trends were graphed using the seaborn function *sns.lineplot*. The musical attributes danceability_% and energy_% were grouped together, as well as valence_% and acousticness_%.

- **Answer**: The first line graph shows that there is a slightly positive correlation between danceability_% and energy_%, as it can be seen that danceability_% increases as energy_% also increases. Meanwhile, there seems to be little to no correlation between valence_% and acousticness_% since there is no clear trend seen in the second line graph.
  
### VI. Platform Popularity
**1. How do the numbers of tracks in spotify_playlists, spotify_charts, and apple_playlists compare? Which platform seems to favor the most popular tracks?**
  - In order to sum the number of tracks using the pandas function *.value_counts()* and *.sum()*, the non-numeric numbers in the columns 'in_spotify_playlists', 'in_spotify_charts', and 'in_apple_playlists' were converted using *pd.to_numeric, errors = coerce*. The resulting data was displayed in a bar plot executed using the matplotlib feature *plt.bar*.

- **Answer**: The bar graph indicates that Spotify Playlists have the most tracks, suggesting Spotify users are more inclined to curate their playlists. Apple Playlists also has a high track count, showing that many users actively engage with this platform. In contrast, Spotify Charts have fewer tracks. Generally, both Spotify and Apple platforms have a significant amount of playlist engagement, but Spotify Playlists seem to be more preferred by the typical listener.
  
### VII. Advanced Analysis
**1. Based on the streams data, can you identify any patterns among tracks with the same key or mode (Major vs. Minor)?**
  - The key and streams columns were grouped together using the *.groupby* feature to show them side-by-side in a dataframe. The total streams for each key were acquired using *.sum()* and the dataframe was organized using *.sort_index()* and *.reset_index()*. Likewise, the same code pattern was used for the mode. These trends in these dataframes were displayed using the matplotlib feature *plt.bar*.

- **Answer**: Based on the first bar graph, C# is the most favored key, with 72.5 billion streams. Meanwhile, D# is the least preferred by listeners, with 18.3 billion streams. Songs with keys B, D, F, G, and G# are also among the most listened to after C#, with over 40 billion streams.

  As seen in the second bar graph, listeners are more inclined to stream tracks with the major mode, with a total of 293.6 billion streams, compared to the minor mode, with 195.8 billion streams. The gap of almost 100 billion indicates that listeners might be more inclined to stream more upbeat, major key tracks.
  
**2. Do certain genres or artists consistently appear in more playlists or charts? Perform an analysis to compare the most frequently appearing artists in playlists or charts.**
- All playlists and charts were grouped together in order to acquire the total sum of appearances for these categories using the pandas function *.sum()*. The top 10 data was sorted in descending order using the features *.sort_values()* and *.head()*. This data was graphed using the bar plot feature in the matplotlib library.

 - **Answer**: The playlists and charts across different are both dominated by the same artists. The Weeknd has a total of 147868 playlist appearances, followed by Taylor Swift with 136478 playlist appearances. On the other hand, Taylor Swift leads the charts with 4277 appearances, followed by The Weeknd with 2405 appearances. This suggests that both entertainers connect with a wide range of audiences regardless of the listening platform. Similarly, Ed Sheeran appears in the top 10 of both categories despite being in different ranks (131908 playlist appearances and 1499 chart appearances), which is still a good indicator of his popularity among listeners across various platforms.
    
**Note: a summary of answers to these questions can be found at the end of my code inside the Jupyter Notebook.**

## Version History
**Version 1.0 - November 7, 2024**
- created *README* file
- uploaded *spotify-2023.csv* dataset

**Version 1.1 - November 9, 2024**
- updated *README* file
- uploaded *Exploratory Data Analysis on Spotify 2023 Dataset - Dayao.ipynb* code

## Authors
Sophia Nicole C. Dayao
<br>
2ECE-C

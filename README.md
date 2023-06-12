# Exploring the Evolution of Hip-Hop: Celebrating 50 Years of the Genre with a Recommender System
---

## Problem Statement
---
The 50th anniversary of hip hop is a significant milestone, and there is a need to celebrate the genre's rich history and help users discover its diverse range of artists and songs.The goal of this project is to develop a spotify recommender system to commemorate the 50th anniversary of the hip hip and help users explore the genre using data science and machine learning techniques. 

The recommender system will analyze various audio features of hip hop songs, such as danceability, energy, valence, and tempo, to understand the musical characteristics that define the genre. It will use a content-based approach, focusing on similarities between songs based on these features, to generate recommendations for users.

### Background Research
Hip hop, as a cultural and musical movement, has had a significant impact on society over the past 50 years. It emerged in the 1970s in the Bronx, New York City, and quickly spread to other regions, becoming a global phenomenon. Understanding the evolution of hip hop across different regions and eras provides valuable insights into its diversity, cultural significance, and influence on music and society.
-source:https://etmonline.org/stories/hiphophistory/
-source:https://timeline.carnegiehall.org/genres/rap-hip-hop

## Data Description
The data was collected from the Spotify API using the Spotipy and includes over 2000 songs and 23 features in total.

## Data Dictionary

cleandf.csv has 2078 observations and 23 features

| Variable Name | Description | Units | Data Type |
| --- | --- | --- | --- |
| `artist` | name of the person/people who performed the song| text | object |
| `album` | name of the project the song is on | text | object |
| `track_name` | name of the song | text | object | 
| `track_id` | unique identifier for every song on Spotify | text/numeric | object | 
| `danceability` | how suitable a track is for dancing | Numeric | float64 |
| `energy` | a measure of intensity and activity | Numeric 0-1 | float64 |
| `key` | The key the track is in | Numeric -1-11 | category |
| `loudness` | The overall loudness of a track in decibels | Numeric | float64 | 
| `mode` |  indicates the major or minor of a track. Major is 1 and minor is 0.| Numeric 0 OR 1 | int64 | 
| `speechiness` | detects the presence of spoken words in a track. An audiobook would be closer to 1 | Numeric 0-1 | float64| 
| `instrumentalness` | Predicts whether a track contains no vocals. The higher the value, the more likely the song is to have no vocals. | Numeric 0-1 | float64 | 
| `liveness` | probability that the track was performed live| Numeric | float64 | 
| `valence` | the musical positiveness conveyed by a track. Higher valence= more positive | Numeric 0-1 | float64 | 
| `tempo` | beats per minute | Numeric | float64 | 
| `duration_ms` | The duration of the track in milliseconds. | Numeric | int64 
| `time_signature` | measure of how many beats are in each bar or measure | Numeric 3-7 | int64 |
| `popularity` | how popular the song is | Numeric 0-100 | string |
| `release_date` | release date of the album the song is on | text | datetime64 | 
| `artist_id` | unique identifier for each artist on Spotify| text/numeric | object | 
| `genres` | list of genres the artist is associated with | text | object|
| `release_year` | year extracted from release_date | Numeric | int64 |  
| `region` | describes the region of the United States that the artist is associated with. Extracted from genres. | text | object | 
| `era` | feature created to group years by different time periods | text/numeric | string | 


## Methodology

### Data Gathering
An existing spotify account was used to log into the Spotify Developer website to access the Spotify Web API. A new app was launched on the Dashboard. This app provides the necessary credentials (CLIENT_ID, CLIENT_ID) to authenticate and access the Spotify API. An .env file was created to securely store the credentials. An example_env.txt file (in the data folder) is included to show how the credentials were stored. The API request was made using the **Spotipy** library.
The playlists were chosen based on the genre and the number of tracks. Multiple functions were created to pull all of the different playlist and artist attributes then combined and saved to a csv. 

### Data Cleaning and EDA
The data was examined to make sure there were no null values and the data was free of special characters. The data was changed to the correct data types. The "region", "eras" , and "release_year" columns were created from the data. 

### Recommender/Modeling
The first recommender system was conducted using all of the numeric features in the data plus the engineered features that were one hot encoded. We utilized cosine similarity to measure the similarity between songs based on the selected audio features. After calculating the similarity matrix, we developed a content-based recommender system. Given a target song, the system identifies the most similar songs based on their feature similarity scores. The second recommender system was conducted using select features that were similar in scale.

### Conclusions and Next Steps
Overall, we were able to create recommender systems using cosine similarity. In conclusion, the similarity scores for the the recommenders were both extremely high even with only having three features for the second recommender. 
In general the data was limiting because I don't know how well this system performs on this genre. In the future, I would incude other genres of music to see if there is more variation. I would also pull more user data so I can have more ways to measure success. 




# Exploring the Evolution of Hip-Hop: Celebrating 50 Years of the Genre with a Recommender
---

## Problem Statement<a id='problem_state'></a>
---
The goal of this project is to develop a spotify recommender system to commemorate the 50th anniversary of the hip hip. 
Hip-hop has evolved and diversified over the years, encompassing various sub-genres, styles, and influential artists. The recommender system aims to help users explore and discover the rich and vibrant world of hip-hop.


### Background Research


## Data Description<a id='data_used'></a>

## Data Dictionary<a id='data_d'></a>

cleandf.csv has 2078 observations and 23 features

| Variable Name | Description | Units | Data Type |
| --- | --- | --- | --- | --- |
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


## Methodology<a id='methodology'></a>

### Data Gathering
An existing spotify account was used to log into the Spotify Developer website to access the Spotify Web API. A new app was launched on the Dashboard. This app provides the necessary credentials (CLIENT_ID, CLIENT_ID) to authenticate and access the Spotify API. An .env file was created to securely store the credentials. An example_env.txt file (in the data folder) is included to show how the credentials were stored. The API request was made using the **Spotipy** library.
The playlists were chosen based on the genre and the number of tracks. Multiple functions were created to pull all of the different playlist and artist attributes then combined and saved to a csv. 

### Data Cleaning and EDA
The data was examined to make sure there were no null values and the data was free of special characters. The data was changed to the correct data types. The "region", "eras" , and "release_year" columns were created from the data. 

### Recommender/Modeling



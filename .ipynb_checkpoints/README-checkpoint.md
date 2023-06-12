# Exploring the Evolution of Hip-Hop: Celebrating 50 Years of the Genre with a Recommender
---

## Problem Statement<a id='problem_state'></a>
---
The goal of this project is to develop a spotify recommender system to commemorate the 50th anniversary of the hip hip. 
Hip-hop has evolved and diversified over the years, encompassing various sub-genres, styles, and influential artists. The recommender system aims to help users explore and discover the rich and vibrant world of hip-hop.


### Background Research


## Data Description<a id='data_used'></a>

## Data Dictionary<a id='data_d'></a>

| Variable Name | Description | Units | Type |
| --- | --- | --- | --- | --- |
| `artist` | name of the person/people who performed the song| text | object |
| `album` | name of the project the song is on | text | object |
| `track_name` | name of the song | text | object | 
| `track_id` | unique identifier for every song on Spotify | text/numeric | object | 
| `danceability` | | Numeric | float64 |
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
| `time_signature` | a notational convention to specify how many beats are in each bar or measure | Numeric 3-7 | int64 |
| `popularity` | how popular the song is | Numeric 0-100 | string |
| `release_date` | release date of the album the song is on | text | datetime64 | 
| `artist_id` | out of pocket expenditures for non-premium medical care | dollars | numeric | 
| `genres` | out of pocket expenditures for over the counter health related spending | dollars |
| `release_year` | year extracted from release_date | Numeric | int64 |
| `artist_id` | item 18h - Educational attainment | text | string |
| `genres` | marital status | text | string |  
| `region` | detailed household summary | text | string | 
| `era` | feature created to group years by different time periods | text | string | 


artist                      object
album                       object
track_name                  object
track_id                    object
danceability               float64
energy                     float64
key                       category
loudness                   float64
mode                         int64
speechiness                float64
instrumentalness           float64
liveness                   float64
valence                    float64
tempo                      float64
duration_ms                  int64
time_signature               int64
popularity                   int64
release_date        datetime64[ns]
artist_id                   object
genres                      object
release_year                 int64
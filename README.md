# Data Modeling with Postgres


## Project Motivation
This project is part of Data Engineering Nanodegree Program by Udacity.
The aim is to create a star schema optimized for queries on song play analysis, using a song and a log datasets given.

## Schema
__Fact Table__
- `songplays` - records in log data associated with song plays
    _songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent_

__Dimension Tables__
- `users` - users in the app
    _user_id, first_name, last_name, gender, level_
    
- `songs` - songs in music database
_song_id, title, artist_id, year, duration_

- `artists` - artists in music database
    _artist_id, name, location, latitude, longitude_

- `time` - timestamps of records in songplays broken down into specific units
    _start_time, hour, day, week, month, year, weekday_

## Installation
As default, the scripts runs on a local instance of Postres, on a database named `studentdb`, with user and password set to `student`.
-  Run `create_tables.py` to create the table structure
-  Run `etl.py` to extract data from the data file and load them into the corresponding tables
-  [Optional] Open `test.ipynb` to test the etl pipeline and query the resulting database


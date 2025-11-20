# Spotify_SQL_Project
This project performs an end-to-end SQL analysis of a Spotify dataset containing detailed information about:  Tracks  Artists  Albums  Musical attributes (danceability, energy, acousticness, tempo, etc.)  Engagement metrics (views, likes, comments, streams)
1. Overview:

This project performs end-to-end SQL analysis on a Spotify dataset containing information about tracks, albums, artists, audio features, engagement metrics, and streaming platforms.

The purpose of the project is to master advanced SQL concepts by working on a real-world dataset.

The project includes data exploration, table creation, writing SQL queries of all difficulty levels, using window functions, joins, CTEs, aggregations, and generating insights.

The dataset contains detailed metrics such as danceability, energy, loudness, tempo, views, likes, comments, and streams.

2. Table Structure:
DROP TABLE IF EXISTS spotify;
CREATE TABLE spotify (
    artist VARCHAR(255),
    track VARCHAR(255),
    album VARCHAR(255),
    album_type VARCHAR(50),
    danceability FLOAT,
    energy FLOAT,
    loudness FLOAT,
    speechiness FLOAT,
    acousticness FLOAT,
    instrumentalness FLOAT,
    liveness FLOAT,
    valence FLOAT,
    tempo FLOAT,
    duration_min FLOAT,
    title VARCHAR(255),
    channel VARCHAR(255),
    views FLOAT,
    likes BIGINT,
    comments BIGINT,
    licensed BOOLEAN,
    official_video BOOLEAN,
    stream BIGINT,
    energy_liveness FLOAT,
    most_played_on VARCHAR(50)
);

3. Data Exploration

The dataset includes three main fields: track-level information, audio attribute information, and engagement information.

Track details include artist name, track name, album name, and album type (single or album).

Audio attributes include danceability, energy, acousticness, instrumentalness, tempo, liveness, loudness, and speechiness.

Engagement information includes views, likes, comments, streaming counts, licensing status, and official video availability.

Data exploration helps understand missing values, column distributions, and potential analytical opportunities.

4. Querying the Data
4.1 Easy Level Queries

Retrieve all tracks with more than one billion streams.

List all albums along with the artists who created them.

Calculate the total number of comments for tracks where the licensed value is TRUE.

Retrieve all tracks where the album type is "single".

Count how many tracks each artist has in the dataset.

4.2 Medium Level Queries

Calculate the average danceability of tracks in every album.

Retrieve the top five tracks that have the highest energy values.

Retrieve track names, views, and likes where official_video is TRUE.

Calculate the total views for every album.

Retrieve track names that have been streamed more on Spotify than YouTube views.

4.3 Advanced Level Queries

Retrieve the top three most-viewed tracks for every artist using window functions.

Retrieve all tracks where the liveness value is greater than the average liveness.

Calculate the difference between the highest and lowest energy values for all tracks in each album using a CTE

Audio attributes include danceability, energy, acousticness, instrumentalness, tempo, liveness, loudness, and speechiness.

Engagement information includes views, likes, comments, streaming counts, licensing status, and official video availability.

Data exploration helps understand missing values, column distributions, and potential analytical opportunities.

5. How to Run This Project

Install PostgreSQL and pgAdmin.

Create a database and run the table schema provided above.

Import the dataset into the table.

Run the queries starting from easy, then medium, then advanced.

Explore additional queries to generate more insights.

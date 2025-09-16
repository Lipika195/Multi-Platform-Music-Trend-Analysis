
 **Multi-Platform-Music-Trend-Analysis**
 
*Project Overview:*

This project analyzes multi-platform music streaming trends (Spotify, Apple, Deezer, Shazam, etc.) using Power BI.
It aims to explore:
Artist & track popularity
Platform contributions & chart presence
Audio feature impact on streams
Time-based trends & comparisons
The Power BI dashboards offer a comprehensive view of streaming performance and help identify growth opportunities for artists, tracks, and platforms.

Dataset
File: Multi-platform Music Data.csv attached in this repository contains 24 columns

*Key Column:*

 track_name – *Track title
 artist_name – *Artist(s)
 Multi-Platform streams* 
 released_year, released_month, released_day – Release date*
 Audio Features : *danceability, energy, valence, BPM
 Playlist/Chart presence across Spotify, Apple, Deezer, Shazam

DAX Measures:

 *Dashboard Features:*

The dashboard contains the following visuals:
 1}Cards (KPIs):Total Streams
             Distinct Artists
             Distinct Tracks
            Average Streams per Day
 2)Bar Chart:Top 10 Artists by Streams:
 3)Matrix Table:Top 10 Tracks with their Energy, Valence, Streams, Danceability
 5)Donut Charts:BPM Distribution
               Platform Share (Spotify, Apple, Deezer, Shazam)
 6)Line Chart:Monthly Streams over time
 7) Column Chart:Relationship between Danceability & Energy of Tracks

 Key Insights
 
 Artist Dominance: A handful of artists drive a large share of total streams.
 Track Characteristics: High-stream tracks often show higher danceability and energy, with balanced valence.
 BPM Distribution: Most popular tracks fall in the 100–140 BPM range.
 Platform Share: Spotify accounts for the majority of streams, with Apple/Deezer/Shazam contributing smaller shares.
 Seasonality: Streaming activity shows noticeable monthly fluctuations.

Conclusion:

This project demonstrates how music streaming trends can be effectively analyzed with Power BI + DAX.
The dashboards provide value to:
Artists – Understand feature-driven success factors
Labels – Optimize promotion strategies across platforms
Analysts – Track industry trends & growth patterns

Tools Used:
Excel-Raw Data Source
Power Query – Data cleaning & transformation
Power BI Desktop – Data Modeling,Dax Measures,Dashboard Creation
GitHub – Project Sharing and Documentation

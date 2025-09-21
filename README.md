
 **Multi-Platform-Music-Trend-Analysis**
 
*Project Overview:*

This project analyzes multi-platform music streaming trends (Spotify, Apple, Deezer, Shazam, etc.) using Power BI.
It aims to explore artist & track popularity, platform contributions & chart presence, audio feature impact on streams, and time-based trends & comparisons
The Power BI dashboard offers a comprehensive view of streaming performance and help identify growth opportunities for artists, tracks, and platforms.

Dataset:

File: Multi-platform Music Data.csv attached in this repository contains 24 columns

*Key Column:*

 track_name – Track title
 
 artist_name – Artist(s)
 
 Multi-Platform streams
 
 released_year, released_month, released_day – Release date
 
 Audio Features : danceability, energy, valence, BPM
 
 Playlist/Chart presence across Spotify, Apple, Deezer, Shazam

Important DAX Measures:

Total Stream = SUM('Streaming Performance Table'[streams])

Avg Streams per Artist = DIVIDE([Total Stream], [Distinct Artists])

Avg Streams per Track = DIVIDE([Total Stream], [Distinct Tracks]) 

Distinct Artists = DISTINCTCOUNT('Artists Table'[Artist_id])

Distinct Tracks = DISTINCTCOUNT('Tracks Table'[Track_id])

Avg Streams per Day = AVERAGEX(VALUES('Calendar Table'[Date]), [Total Stream])

Previous Month Streams = 
CALCULATE(
    [Total Stream],
    DATEADD('Calendar Table'[Date], -1, MONTH))
    
Previous Year Streams = 
CALCULATE (
    [Total Stream],
    DATEADD ( 'Calendar Table'[Date], -1, YEAR ))
    
 Rolling 7 Day Streams = 
CALCULATE(
    [Total Stream],
    DATESINPERIOD(
        'Calendar Table'[Date],
        MAX('Calendar Table'[Date]),
        -7,
        DAY))

   Avg BPM = AVERAGE('Audio Features Table'[bpm])

   Avg Danceability = AVERAGE('Audio Features Table'[danceability_%])

   Avg Energy = AVERAGE('Audio Features Table'[energy_%])


 *Dashboard Features:*

The dashboard contains the following visuals:
 1}Cards (KPIs):Total Streams
             Distinct Artists
             Distinct Tracks
            Average Streams per Day
            
 2)Bar Chart:Top 10 Artists by Streams
 
 3)Matrix Table:Top 10 Tracks with their Energy, Valence, Streams, Danceability
 
 5)Donut Charts:BPM Distribution
               Platform Share (Spotify, Apple, Deezer, Shazam)
               
 6)Line Chart:Monthly Streams over time
 
7)Column Chart:Relationship between Danceability & Energy of Tracks

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
Analysts – Track industry trends & growth patterns.

Tools Used:

Excel-Raw Data Source

Power Query – Data cleaning & transformation

Power BI Desktop – Data Modeling,Dax Measures,Dashboard Creation

GitHub – Project Sharing and Documentation

---
layout: post
title: DMV Music Database
description: A SQL Database highlighting DMV's musicians and trends
---

This unique database highlights the achievements of 30 solo artists and 60 bands from the Washington, D.C. area, covering genres like go-go, jazz, rap, R&B, and punk rock, to increase their global recognition and showcase music trends over the last four decades.

**The database consists of 11 tables with the following structure:**

1. Main Tables:
      * Bands and Artists
3. Reference Tables:
      * Instruments
      * Record Labels
      * Albums
3. Linking Tables:
      * Band_instruments
      * Label_bands
      * Label_artists
      * Artist_instruments
      * Artist_albums

**The database includes various one-to-many relationships among all tables.**

### Logical Design ###

<img src="/assets/images/image_ERD.png" width=500 alt="Picture of ERD Diagram">

The database design ensures information is presented clearly and intuitively. The ERD tables capture essential details about artists, their albums, record labels, and instruments. By separating properties for artists and bands, the design remains organized and uncluttered. This structure makes it easy to understand table relationships and key connections.

### Sample Data ###

Facing a lack of existing datasets, my team and I compiled data from [DC Artists](www.last.fm/tag/dc/artists){:target="_blank"}, [DMV Artists](www.last.fm/tag/dmv/artists){:target="_blank"}, and [Top DMV Artists](www.dmvlife.com/dmvartists.html){:target="_blank"}
 and DMV Life, using tags for "DMV" and "DC" artists. Due to the formatting of these websites, we had to manually compile this data ourselves in individual .csv files. Key details gathered included artist/band names, album names, record label names, records sold, years active, genres, and types of instruments used. This data was structured into 11 tables covering 30 solo artists, 60 bands, 433 albums, and 55 record labels in our database.

### Glimpse of the Tables ###

`This depicts the main table of "Bands"`


<img src="/assets/images/band_table.png" width=500 alt="Picture of Bands table">

`This depicts the main table of "Artists"`

<img src="/assets/images/artist_table.png" width=500 alt="Picture of Artists table">

`This depicts the reference table of "Instruments"`

<img src="/assets/images/instrument_table.png" height="450" alt="Picture of Instruments table">

`This depicts the reference table of "Albums"`

<img src="/assets/images/album_table.png" height="450" alt="Picture of Albums table">

`This depicts the linking table of "Band_instruments"`

<img src="/assets/images/band_instruments_table.png" height="450" alt="Picture of Band_instruments table">



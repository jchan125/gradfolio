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

![ERD_Diagram](https://github.com/jchan125/gradfolio/blob/master/assets/images/image_ERD.png?raw=true)

The database design ensures information is presented clearly and intuitively. The ERD tables capture essential details about artists, their albums, record labels, and instruments. By separating properties for artists and bands, the design remains organized and uncluttered. This structure makes it easy to understand table relationships and key connections.

### Sample Data ###

Facing a lack of existing datasets, my team and I compiled data from Last FM and DMV Life, using tags for "DMV" and "DC" artists. Due to the formatting of these websites, we had to manually compile this data ourselves in individual .csv files. Key details gathered included artist/band names, album names, record label names, records sold, years active, genres, and types of instruments used. This data was structured into 11 tables covering 30 solo artists, 60 bands, 433 albums, and 55 record labels in our database.

### Glimpse of the Tables###

`This depicts the main table of "Band"`

![band_table](https://github.com/jchan125/gradfolio/blob/master/assets/images/band_table.png?raw=true)

`This depicts the main table of "Artists"`

![artists_table](https://github.com/jchan125/gradfolio/blob/master/assets/images/artist_table.png?raw=true)

`This depicts the reference table of "Instruments"`

![instruments_table](https://github.com/jchan125/gradfolio/blob/master/assets/images/instrument_table.png?raw=true)

`This depicts the reference table of "Albums"`

![album_table](https://github.com/jchan125/gradfolio/blob/master/assets/images/album_table.png?raw=true)

`This depicts the linking table of "Band_instruments"`

![band_instruments_table](https://github.com/jchan125/gradfolio/blob/master/assets/images/band_instruments_table.png?raw=true)









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

![ERD_Diagram](https://github.com/jchan125/gradfolio/blob/master/assets/images/image_ERD.png)

The database design ensures information is presented clearly and intuitively. The ERD tables capture essential details about artists, their albums, record labels, and instruments. By separating properties for artists and bands, the design remains organized and uncluttered. This structure makes it easy to understand table relationships and key connections.


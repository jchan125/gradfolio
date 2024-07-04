---
layout: post
title: Analyzing Crime Trends and Enhancing Safety in Urban Areas
description: This project analyzes crime rates at Washington D.C. bus stops to enhance rider safety by pinpointing high-crime areas and proposing security improvements.
---

1st Dataset Used: [Crime Incident Reported (DC)](https://opendata.dc.gov/datasets/DCGIS::crime-incidents-in-2022/about){:target="_blank"}.

2nd Dataset Used: [Metro Bus Stops (DC)](https://opendata.dc.gov/datasets/DCGIS::metro-bus-stops-2/about){:target="_blank"}.

### Introduction ###

With the rise in violent crimes, there's a need to analyze current preventative measures and resource allocation, particularly at bus stops in urban areas like the DMV. This project aims to identify wards with the highest crime rates and assess trends in resource allocation, focusing on bus stops.

`The Analyzed Characteristics of Each Dataset`
1. Crime Incidents 2022
* Ward
* Shift (time of day)
* Offense types include auto theft, motor vehicle theft, robbery, assault with a dangerous weapon, burglary, homicide, sex abuse, and arson

2. Metro Bus Stops
* Service effective dates for each ward
* Presence of street lights within 30 feet
* Street locations

`Outcome:` Identify wards with high crime rates, and provide recommendations for resource reallocation to improve bus stop safety..

### Method ###

The datasets were merged to find correlations between bus stop locations and crime rates. Visualizations were created to identify wards with high crime rates and inadequate resource allocation. Based on these findings, suggestions were provided for reallocating preventative services to enhance bus stop safety.

Python Libraries Used:
* Pandas
* Matplotlib
* Folium


~~~
offenses_day = crime_bus_df.groupby(['WARD', 'TIME'])['OFFENSE'].size().reset_index()
offenses_day.pivot(index = 'WARD', columns = 'TIME', values = 'OFFENSE').plot(kind='bar')
plt.xlabel('WARD')
plt.ylabel('Number of Offenses')
plt.title('Number of Offenses by Time of Day')
plt.show()
~~~

~~~cpp
offenses_day = crime_bus_df.groupby(['WARD', 'TIME'])['OFFENSE'].size().reset_index()
offenses_day.pivot(index = 'WARD', columns = 'TIME', values = 'OFFENSE').plot(kind='bar')
plt.xlabel('WARD')
plt.ylabel('Number of Offenses')
plt.title('Number of Offenses by Time of Day')
plt.show()
~~~

### An H3 header ###

Now a nested list:

 1. First, get these ingredients:

      * carrots
      * celery
      * lentils

 2. Boil some water.

 3. Dump everything in the pot and follow
    this algorithm:

        find wooden spoon
        uncover pot
        stir
        cover pot
        balance wooden spoon precariously on pot handle
        wait 10 minutes
        goto first step (or shut off burner when done)

    Do not bump wooden spoon or it will fall.

Notice again how text always lines up on 4-space indents (including
that last line which continues item 3 above).

Here's a footnote [^1].

[^1]: Some footnote text.

Tables can look like this:

| Header 1 | Header 2                   | Header 3 |
|:--------:|:--------------------------:|:--------:|
| data1a   | Data is longer than header | 1        |
| d1b      | add a cell                 |          |
| lorem    | ipsum                      | 3        |
|          | empty outside cells        |          |
| skip     |                            | 5        |
| six      | Morbi purus                | 6        |


A horizontal rule follows.

***

Here's a definition list:

apples
  : Good for making applesauce.

oranges
  : Citrus!

tomatoes
  : There's no "e" in tomatoe.

Again, text is indented 4 spaces. (Put a blank line between each
term and  its definition to spread things out more.)

Here's a "line block" (note how whitespace is honored):

| Line one
|   Line too
| Line tree

and images can be specified like so:

![example image](https://images.unsplash.com/photo-1488190211105-8b0e65b80b4e?w=300&h=300&fit=crop "An exemplary image")

Inline math equation: $\omega = d\phi / dt$. Display
math should get its own line like so:

$$I = \int \rho R^{2} dV$$

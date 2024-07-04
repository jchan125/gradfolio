---
layout: post
title: Analyzing Crime Trends and Enhancing Safety in Urban Areas
description: This project analyzes crime rates at Washington D.C. bus stops to enhance rider safety by pinpointing high-crime areas and proposing security improvements.
---

Dataset Used: [here](https://opendata.dc.gov/datasets/DCGIS::crime-incidents-in-2022/about){:target="_blank"}.

**Introduction**
With the rise in violent crimes, there's a need to analyze current preventative measures and resource allocation, particularly at bus stops in urban areas like the DMV. This project aims to identify wards with the highest crime rates and assess trends in resource allocation, focusing on bus stops.

`Objective:`
 * Enhance safety at bus stops by reallocating resources such as security personnel, street lights, and cameras.

`Importance:` 
 * Prioritize rider safety due to the benefits and reliability of buses as a mode of commute.

'Datasets Used:'
Crime Incidents 2022:
Analyzed characteristics: 
* Ward
* Shift (time of day)
* Offense type

`Offenses"
* Auto theft
* Motor vehicle theft
* Robbery
* Assault with a dangerous weapon
* Burglary
* Homicide
* Sex abuse
* Arson

`Metro Bus Stops:`
* Service effective dates
* Presence of street lights within 30 feet
* Street locations.


`Outcome:` Identify wards with high crime rates, and provide recommendations for resource reallocation to improve bus stop safety..

> Block quotes are
> written like so.
>
> They can span multiple paragraphs,
> if you like.


H2 Header
------------

Here's a numbered list:

 1. first item
 2. second item
 3. third item

Note again how the actual text starts at 4 columns in (4 characters
from the left side). Here's a code sample:

    # Let me re-iterate ...
    for i in 1 .. 10 { do-something(i) }

As you probably guessed, indented 4 spaces. By the way, instead of
indenting the block, you can use delimited blocks, if you like:

~~~
define foobar() {
    print "Welcome to flavor country!";
}
~~~

(which makes copying & pasting easier). You can optionally mark the
delimited block for Pandoc to syntax highlight it by specifying the languagae after the start of a block (e.g. `~~~cpp`) which would look like :

~~~cpp
#include <iostream>
using namespace std;

int main() 
{    
    cout << "Size of char: " << sizeof(char) << " byte" << endl;
    cout << "Size of int: " << sizeof(int) << " bytes" << endl;
    cout << "Size of float: " << sizeof(float) << " bytes" << endl;
    cout << "Size of double: " << sizeof(double) << " bytes" << endl;

    return 0;
}
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

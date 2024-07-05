---
layout: post
title: WSTC Missed Trips Analysis
description: My Capstone project analyzing bus ridership for equitable transport in Maryland
---

The mission of the Washington Suburban Transit Commission (WSTC) is to enhance public transportation services and infrastructure in Montgomery County and Prince George's County, Maryland, with a focus on promoting efficient, accessible, and sustainable mass transit options. This project analyzes bus ridership data related to missed trips from three bus service providers: WMATA, Ride On, and The Bus. It also examines these missed trips in relation to Equity Emphasis Areas, which are regions with high concentrations of low-income individuals and/or traditionally disadvantaged racial and ethnic groups. The project aims to provide insights to the WSTC on factors contributing to missed trips, supporting their mission to improve transportation services for underprivileged communities.

*To protect sensitive information such as specific bus routes, EventType names, other sensitive information, and values they have been anonymized per security guidelines by hiding x and y values using the following code:*

~~~python
plt.gca().axes.get_xaxis().set_visible(False)
plt.gca().axes.get_yaxis().set_visible(False)
~~~

*This summary maintains the project's focus and goals while ensuring that sensitive information is safeguarded*

### I worked as the Project Manager and Data Analyst on this project and will be presenting a small snippet of the work that I have contributed ###
I utilized Trello for work breakdown structure and to track our progress on this project, organized deliverables into weekly sprints, and presented updates biweekly to our client's representative. 

`Primary Coding Environments`
* Python as the primary programming language
* Visual Studio Code for the environment
* Jupyter Notebook for deliverables 

`Key packages`
* Pandas for data cleaning
* Matplotlib for visualizations
* ArcGIS Online for mapping

### Code Examples with Outputs ###
*Variable names and code have been edited for anonymity*

~~~python
Bus_Depot_Monthly = Bus_Depot.groupby(Bus_Depot['Date'].dt.month).size()
Bus_Depot_Monthly.plot(kind="bar")
plt.xlabel('Month in the Year')
plt.ylabel('Number of Missed Trips')
plt.title('Missed Trips Breakdown By Month')
plt.xticks(rotation=0)
plt.show()
~~~
<img src="https://github.com/jchan125/gradfolio/blob/master/assets/images/count_month.png?raw=true" width=500 alt="Total Missed Trips per Month">

As you can see, the month of January (1) had a lot of missed trips. To further investigate whether this was an outlier, I needed to see the breakdown of why trips were being missed in that month.

~~~python
Depot_EventTypes = Bus_Depot.groupby('EventType').size().sort_values(ascending=False)
plt.style.use('default')
Depot_EventTypes.plot(kind='barh')
plt.title('Counts for Each Event Type')
plt.tight_layout()
plt.xlabel('Number of Occurrences')
plt.show()
~~~
<img src="https://github.com/jchan125/gradfolio/blob/master/assets/images/count_eventType.png?raw=true" width=500 alt="Count of EventTypes">

One event type stood out as significantly larger than the others, explaining why trips were being missed. Now, I want to determine if this variable contributed to the high number of missed trips in January.

~~~python 
plt.figure(figsize=(12, 6))
Depot_EventTypes.plot(kind='bar', position=0, label='With January', width=0.4)
Depot_EventTypes_Exclude_Jan.plot(kind='bar', color='orange', position=1, label='Without January', width=0.4)
plt.title('Counts for Each Event Type')
plt.ylabel('Number of Occurrences')
plt.legend()
plt.tight_layout()
plt.show()
~~~
<img src="https://github.com/jchan125/gradfolio/blob/master/assets/images/jan_EventType.png?raw=true" width=500 alt="Count of EventTypes For January">

The primary event type observed in the previous graph correlates with the high incidence seen in January. This suggests that the data for January slightly influences or skews the overall analysis.

~~~python
Depot_Specific_Problems = Bus_Depot[Bus_Depot['EventType'] == 'Specific Event Type']
Depot_Specific_Group = Depot_Specific_Problems.groupby('Specific Event Type').size().sort_values(ascending=False)
Depot_Specific_Group.plot(kind='barh')
plt.title('Counts for Each Problem')
plt.xlabel('Number of Occurrences')
plt.tight_layout()
plt.show()
~~~
<img src="https://github.com/jchan125/gradfolio/blob/master/assets/images/count_problem.png?raw=true" width=500 alt="Count of a Specific Problem">

This graph shows the second-highest event type contributing to missed trips for this specific bus and depot, with a slightly more varied distribution of data.

~~~python
Depot_Total_MissedTrips = Bus_Depot.groupby(Bus_Depot['Route']).size().sort_values(ascending=False)
plt.figure(figsize=(15, 8))
Depot_Total_MissedTrips.plot(kind='bar', width=0.8)
plt.title('Total Missed Trips by Route')
plt.gca().axes.get_xaxis().set_visible(False)
plt.ylabel('Number of Missed Trips')
plt.tight_layout()
plt.show()
~~~
<img src="https://github.com/jchan125/gradfolio/blob/master/assets/images/count_route.png?raw=true" width=500 alt="Total Missed Trips by Route">

This visualizes the total number of missed trips for each route number.

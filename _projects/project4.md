---
layout: post
title: WSTC Missed Trips Analysis
description: My Capstone project analyzing bus ridership for equitable transport in Maryland
---

The mission of the Washington Suburban Transit Commission (WSTC) is to enhance public transportation services and infrastructure in Montgomery County and Prince George's County, Maryland, with a focus on promoting efficient, accessible, and sustainable mass transit options. This project analyzes bus ridership data related to missed trips from three bus service providers: WMATA, Ride On, and The Bus. It also examines these missed trips in relation to Equity Emphasis Areas, which are regions with high concentrations of low-income individuals and/or traditionally disadvantaged racial and ethnic groups.

*To protect confidentiality, sensitive information such as specific bus routes, names, and operator numbers has been omitted or anonymized per security guidelines. The project aims to provide insights to the WSTC on factors contributing to missed trips, supporting their mission to improve transportation services for underprivileged communities.*

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
Depot_EventTypes = Bus_Depot.groupby('EventType').size().sort_values(ascending=False)
plt.style.use('default')
Depot_EventTypes.plot(kind='barh')
plt.title('Counts for Each Event Type')
plt.tight_layout()
plt.gca().axes.get_yaxis().set_visible(False) #to hide EventTypes
plt.xlabel('Number of Occurrences')
plt.show()
~~~
<img src="https://github.com/jchan125/gradfolio/blob/master/assets/images/count_eventType.png?raw=true" width=500 alt="Count of EventTypes">

~~~python 
plt.figure(figsize=(12, 6))
Depot_EventTypes.plot(kind='bar', position=0, label='With January', width=0.4)
Depot_EventTypes_Exclude_Jan.plot(kind='bar', color='orange', position=1, label='Without January', width=0.4)
plt.title('Counts for Each Event Type')
plt.ylabel('Number of Occurrences')
plt.legend()
plt.gca().axes.get_xaxis().set_visible(False)
plt.tight_layout()
plt.show()
~~~
<img src="https://github.com/jchan125/gradfolio/blob/master/assets/images/jan_EventTypes.png?raw=true" width=500 alt="Count of EventTypes">

~~~python
Depot_Specific_Problems = Bus_Depot[Bus_Depot['EventType'] == 'Specific Event Type']
Depot_Specific_Group = Depot_Specific_Problems.groupby('Specific Event Type').size().sort_values(ascending=False)
Depot_Specific_Group.plot(kind='barh')
plt.title('Counts for Each Problem')
plt.xlabel('Number of Occurrences')
plt.gca().axes.get_yaxis().set_visible(False)
plt.tight_layout()
plt.show()
~~~
<img src="https://github.com/jchan125/gradfolio/blob/master/assets/images/counts_specific_problem.png?raw=true" width=500 alt="Count of EventTypes">

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
<img src="https://github.com/jchan125/gradfolio/blob/master/assets/images/count_route.png?raw=true" width=500 alt="Count of EventTypes">

~~~python
Bus_Depot_Monthly = Bus_Depot.groupby(Bus_Depot['Date'].dt.month).size()
Bus_Depot_Monthly.plot(kind="bar")
plt.xlabel('Month in the Year')
plt.ylabel('Number of Missed Trips')
plt.title('Missed Trips Breakdown By Month')
plt.gca().axes.get_yaxis().set_visible(False)
plt.xticks(rotation=0)
plt.show()
~~~
<img src="https://github.com/jchan125/gradfolio/blob/master/assets/images/count_month.png?raw=true" width=500 alt="Count of EventTypes">

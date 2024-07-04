---
layout: post
title: WSTC Missed Trips Analysis
description: My Capstone project analyzing bus ridership for equitable transport in Maryland
---

The mission of the Washington Suburban Transit Commission (WSTC) is to enhance public transportation services and infrastructure in Montgomery County and Prince George's County, Maryland, with a focus on promoting efficient, accessible, and sustainable mass transit options. This project analyzes bus ridership data related to missed trips from three bus service providers: WMATA, Ride On, and The Bus. It also examines these missed trips in relation to Equity Emphasis Areas, which are regions with high concentrations of low-income individuals and/or traditionally disadvantaged racial and ethnic groups.

*To protect confidentiality, sensitive information such as specific bus routes, names, and operator numbers has been omitted or anonymized per security guidelines. The project aims to provide insights to the WSTC on factors contributing to missed trips, supporting their mission to improve transportation services for underprivileged communities.*

*This summary maintains the project's focus and goals while ensuring that sensitive information is safeguarded*

### I worked as the Project Manager and Data Analyst on this project and will be presenting the work that I have contributed ###
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


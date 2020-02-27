# DSI client project 5: Projecting Wage Losses Created by Hurricanes

_Authors: Robert Davison, Ata Acka, Karim Jooma

---

## Executive Summary

Natural disasters cause significant damage across the U.S. every year. When a disaster strikes, quite often people are unable to go to work for a temporary period of time. This can be for a number of reasons such as flooding blocking the road to work, power outages at the office, etc. When this happens, people are entitled to insurance reimbursments that compensate a portion of these lost wages. A tool for predicting wage losses could provide real time support in future disasters, but currently one does not exist. This report seeks to develop a baseline model for estimating total wage losses caused by hurricanes.

Unemployment insurance weekly claims data from the department of labor show dramatic spikes directly following major hurricanes which correspond to total jobs temporarily lost. After determining the size of the spike, a rough estimate of total wage loss can be back calculated out. This report presents a prototype model for estimating the number of unemployment claims following a hurricane that is trained from the sizes of spikes caused by 6 past major hurricanes. 
 
Employment, disaster and wage data were gathered from from FEMA's website as well as the U.S. Bureau of Labor Statistics and department of labor.

---

## Data Dictionary

|Column Name|Type|Description|
|---|---|---|
|disaster_number|int|Unique event number used to designate the event|
|title|object|The title of the disaster|
|disaster_type|object|Two character code that defines the type of disaster|
|incident_begin_date|datetime|The date the disaster started|
|incident_duration_days|int|The number of days the disaster took place|
|state|object|The two letter code to indicate the affected state|
|employed|int|Workforce population in the indicated state|
|avg_wagee_per_hour|float|The average wage per hour per state|
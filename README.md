<p align="center">
  <img width="200" height="200" src="https://media-exp1.licdn.com/dms/image/C4E03AQFr1viytj_VQA/profile-displayphoto-shrink_200_200/0?e=1597881600&v=beta&t=5PTBuTdNqtTcUbtcfeRLDowPjvtODnUS1q7lS8NrY4g">
</p>

<h3 align="center">Bijan's Portfolio</h3>

<p align="center">
  Hello world, thanks for stoping by my personal Github.
  <br>
  Below you'll find background on myself and the projects I have worked on over the years.
</p>

## Table of Contents 

- [AEG](#aeg)
- [EY](#ey)
- [NFL](#nfl)

## AEG: Ticketing Application
AEG is one of the largest companies in the live entertainment industry, they book shows at venues and generate revenue from ticket sales. 

The objectives of the AEG Ticketing Application are to first ingest ticket sale data from 3rd parties then associate it with events created in external booking applications.

Below are several features which I enjoyed implementating for this application

#### Ticket Sales ETL 
![screenshot](assets/img/Presentation2.jpg)
Everytime tickets are sold for an AEG show raw ticket sale data from 3rd parties is sent to AEG's datawarehouse.

The raw data is then available for the Ticketing Application to ingest, upon import the raw data is transformed to the intermediate ```ticket_feed_wrap``` table.

The ```ticket_feed_wrap``` tables are then transformed and split into their target tables ```ticket_events``` and ```daily_counts```. 

I was responsible for defining the tables required at each step of the transformation, along with testing the outcome of the Ticket Sales ETL. 

See documentation below for details: 

[Ticketing ETL Product Requirements](https://github.com/bayrami1/work-experience-/blob/master/AEG%20Project/ETL%20Product%20Requirements%20.pdf)

#### Matching Ticket Events to Events in different applications
Everytime a ticket sale is imported into the Ticketing App BE new ```ticket_events``` and ```daily_counts``` objects are created. 

At AEG they used different applications to create ```booking_events``` which could be associated with a ```ticket_event``` created in the Ticketing Application. 

As a result we had to create another ETL to import ```booking_events``` from different applications store them on our BE and create an intuitive workflow that would allow users to use an interface to make the association between the events. 

The first step requires standardizing the ```booking_events``` created in other systems and import them into our backend, which is covered in the documentation below: 



#### Access Control and Privacy Settings
Talk about how it took a lot of user interviews and because it directly impacted business it had to be approved by key stakeholders and product council. 

## EY
#### Storage Manager 
Due to the proprietary data for this project I am unable to share documentation or architecture relating to the project 
- created SM, which was created to manage very sensitive Tax data 
- accomplished using a proprietary cloud agnostic architecture using multiple services 
- created the Tax application which used tokens generated by the storage manager to access sensitive data and automate tax pipelines which were done manually in the past
- the creation of the storage manager and the automated pipelines ran through the tax application allowed the Tax team to increase efficiency of their team by 25%

## NFL 
#### Fantasy Football Data Analysis Project

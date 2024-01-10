<!--
<p align="center">
  <img width="200" height="200" src="https://media-exp1.licdn.com/dms/image/C4E03AQFr1viytj_VQA/profile-displayphoto-shrink_200_200/0?e=1597881600&v=beta&t=5PTBuTdNqtTcUbtcfeRLDowPjvtODnUS1q7lS8NrY4g">
</p>
-->
<h3 align="center">Bijan's Portfolio</h3>

<p align="center">
  <br>
  Below I have included background information on the Ticketing Application (TA) I built for the Anschutz Entertainment Group (AEG) while I was working at Kunai Consulting as a Techincal Project Manager. I have also included some examples of the technical documentation I created for the developers on the prtoject as well as other internal technical and non-technical teams. 

<p align="center">
The Anschutz Entertainment Group, with 11,000 employees and an annual revenue of $20B as of 2022, considers this application crucial to their business. Successfully delivering it ranks among my greatest accomplishments. 

</p>

## AEG Ticketing Application and Reporting Platform 
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

[Ticketing ETL Documentation](https://github.com/bayrami1/work-experience-/blob/master/AEG%20Project/ETL%20Product%20Requirements%20.pdf)

#### Matching Ticket Events to Events in different applications
Everytime a ticket sale is imported into the Ticketing App backend a new ```ticket_events``` and ```daily_counts``` objects are created, these tables represent the ticket sales associated with a given show or ```booking_events``` created in AEGs booking applications.   

The second objective of the Ticketing Application is too associate ```ticket_events``` with ```booking_events```, for reporting and forecasting. 

![screenshot](assets/img/Event_ID_association.jpg)

The first step required standardizing the raw ```booking_events``` created in other systems and then importing them from a datawarehouse into our backend. 

![screenshot](assets/img/match_events.jpg)

The second step required creating an intuitive workflow that would allow users to easily make the association between Ticket Events and Booking Events (NOTE: there are no recommended booking events for the given ticket events in the screenshot above because we were using test data) 

Successfully delivering this feauture required working closely with engineering, UX, and business teams. Collaborating with a  cross-functional team to deliver a complex feature is what made shipping this feature so fulfulling. 

See documentation below for more details: 

[Booking Events Import Documentation](https://github.com/bayrami1/work-experience-/blob/master/AEG%20Project/booking_events%20documentation%20.pdf)

#### Access Control and Privacy Settings
Defining the roles for this application took extensive user interviews, there was only one role in the last application they used and this led to major issues between business units. 

I added a ticketer role, and groups which limited the events users had access too which greatly reduced the amount of friction between business units. 

The documentation below outlines the roles and respective priviliges, and the list groups used. The appendix also includes outlines for the user stories required to implement the roles and privacy settings:

[Access Control and Privacy Settings Documentation](https://github.com/bayrami1/work-experience-/blob/master/AEG%20Project/TA%20_%20Access%20Control%20and%20Privacy%20Settings.pdf)


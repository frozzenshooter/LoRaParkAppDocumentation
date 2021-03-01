# Activity diagrams

This folder contains the relevant activity diagrams for the LoRaPark app. 
The activites are splitted into several smaller ones: 

* Rule update
* Rule activiation
* Rule deactivation
* Server chache update + Event creation
* Event handling and rule evaluation

Reason for the event creation on the serverside (by calculating the delta) is, that the used API to access the sensor data doesn't provide an event based access method. 
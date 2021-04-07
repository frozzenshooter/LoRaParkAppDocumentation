# LoRaParkAppDocumentation

This repository contains the documentation for the LoRaPark App and the coresponding server.

The application uses rules to execute an action, like an notification, when a condition is evaluates as true. The condition is based on sensor values, which will the application obtain from the server.

The [server](https://github.com/oli-f/LoRaParkServer) acts as middleware between the sensor data API and the [android application](https://github.com/frozzenshooter/LoRaParkApplication). It offers a REST-API for the application that will offer the sensor data. The sensor data will be chached and refresh in a certain time interval.

More details about the innner workings can be found in the [activity diagrams](./ActivityDiagrams).

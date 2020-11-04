# CPSC449-Project4
# Authors: 
Mauricio Macias (mauricio.macias@csu.fullerton.edu) 890741622 <br/>
Andrew Dinh	(decayingapple@csu.fullerton.edu) 893242255 <br/>
Ariosto Kuit 	(Ariostokuitak@csu.fullerton.edu) 889834065 <br/>

## 0 Installation
Make sure you are in the project root and run:

"foreman start -m "gateway=1,users=3,timelines=3"

## 1 Background 

For this project we will add more features to our microservices. For project 2 we noticed that each service is on a different port, there is only one instance of each service, and only have one authentication call to the entire system. So we will fix these issues by introducing an API gateway to mediate between users and our services

This project was completed by 3 people. Whose names are listed in the very top of this paper.

## 2 Using Project 2 Services

For this project we will use the repository from project 2 to build upon for this project.The Procfile is updated to be able to use our services.

## 3 Adding a Gateway 

In our project we are going to add an API gateway to manage the client with our backend microservices. We use foreman to start the gateway and services. When using foreman to start the gateway, it will successfully access to port 5000 for our services.

## 4 Routing

In our Routing we will route request to port 5000 for different resources to an instance of the correct microservice. 

## 5 Load Balancing
For our load balancing we will apply a very simple load balance policy: round-robin to control traffic distrution to our microservices. The routes.cfg file is edited with the addresses of all three instances of each service. The file gateway.py is modified to forward requests to each instance. We also restart the foreman with --formation switch which starts an instance of the gateway and threee instances of each microservice.

## 6 Authentication

For our project we are going to add the functionally that every API calls require HTTP Basic authentication. Our project uses Flask-BasicAuth to handle authentication. Flask-BasicAuth is also used to request header and produce WWW-Authenticate: the response header. The API should return true when we pass it through the authenticateUser(username, password) function, otherwise it will return HTTP 401.

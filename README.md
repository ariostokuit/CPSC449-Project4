# CPSC449-Project4
# Authors: 
Mauricio Macias (mauricio.macias@csu.fullerton.edu) 890741622 <br/>
Andrew Dinh	(decayingapple@csu.fullerton.edu) 893242255 <br/>
Ariosto Kuit 	(Ariostokuitak@csu.fullerton.edu) 889834065 <br/>

## 0 Installation
Make sure you are in the project root and run:

"foreman start"

## 1 Background 

For this project we will add more features to our microservices. For project 2 we noticed that each service is on a different port, there is only one instance of each service, and only have one authentication call to the entire system. So we will fix these issues by introducing an API gateway to mediate between users and our services

This project was completed by 3 people. Whose names are listed in the very top of this paper.

## 2 Using Mockroblog

For this project we will use Mockroblog which our professor made for us to play around with and to help us do this project. 

## 3 Adding a Gateway 

In our project we are going to add an API gateway to manage the client with our backend microservices. We use foreman to start the gateway and services. 

## 4 Routing

In our Routing we will route request to port 5000 for different resources to an instance of the correct microservice. 

## 5 Load Balancing

For our load balancing we will apply a very simple load balane policy: round-robin to control traffic distrution to our microservices. 

## 6 Authentication

For our project we are going to add the functionally that every API calls require HTTP Basic authentication. 

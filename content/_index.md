+++
title = "Refactor Your Data & Workflows"
date = 2021
weight = 1
chapter = false
+++
# Refactor Your Data & Workflows

#### Oveview

In our fictitious TravelBuddy web application, we stored all of our application data in a MySQL database hosted in Amazon RDS. But as we migrate to a microservices architecture, we need to consider breaking this monolithic database up into smaller pieces. This also gives us the opportunity to choose the right datastore for the way our data needs to be accessed - and embrace Polyglot Persistence.

We will create a new microservice that exposes trip sector information so that clients can query for ‘all trips’ or ‘trips from city’. This could be used in the scenario where our clients may want to know what cities can be reached from a given origin. As an optional Challenge Exercise, you are tasked with extending this functionality to also provide the ability to search for flights that are destined for a particular city.

Instead of storing this information in a relational database, we will use the Amazon DynamoDB service. In this lab we will take a look at how to access Amazon DynamoDB from Java using the AWS SDK for Java, hosted in AWS Lambda.

We will then turn our attention to AWS Step Functions and experiment with creating state machines to create managed workflows. The state machine will call Lambda functions to perform tasks.

#### Content:


1. [Introduction](1-introduction/)
2. [Preparation](2-prepare/)
3. [Create A Scan & Query Microservice](3-create-scan-query-microservice/)
4. [Automate Your Microservice](4-automate-microservice/)
5. [Create an API For Your Microservice](5-create-microservice-api/)
6. [Challenge - Enhance The TripSearch Microservice](6-challenge-enhance-tripsearch/)
7. [Create A Calculator Microservice using AWS Step Functions](7-calculator-microservice/)
8. [Challenge - Enhance The Calculator Service](8-challenge-enhance-calculator-service/)
9. [Challenge - Implement An Image Manager Workflow](9-challenge-enhance-imagemanager/)
10. [Clean up resources](10-cleanup/)
+++
title = "Configure Authentication, Authorization and Accounting (AAA)"
date = 2020
weight = 4
chapter = false
pre = "<b>4. </b>"
+++

#### Overview

Right now, our TravelBuddy SPA does not require any authentication in order to call the API services we have exposed. The lab setup process has provisioned a Cognito User Pool and a Cognito Identity Pool in your account. The Cognito User Pool is your fully-managed system of record for users in your application. The Identity Pool is used to obtain temporary AWS IAM credentials to sign requests that require SigV4 signing. The Cognito Identity Pool federates between multiple Identity Providers, but in our lab example, we only have one Identity Provider (the User Pool). Our TravelBuddy SPA does not actually have the requirement for IAM credentials, but we have implemented the feature to demonstrate how you can accomplish this. As a Challenge Exercise, we will ask you to implement AWS IAM Authorisation for a call into API Gateway, but this is an optional task for the lab.


#### Content:
1. [Add Authentication to the SPA using Amazon Cognito User Pools](4.1-add-authentication-with-cognito/)
2. [Setting Up Authentication For The Microservice](4.2-setup-authentication/)
3. [Deploy And Test](4.3-deploy-and-test/)
4. [Add New User Sign Up and Sign In](4.4-add-new-user-signup_signin/)
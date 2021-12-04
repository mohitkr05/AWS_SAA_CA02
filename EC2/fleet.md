# EC2 Fleet

# Table of Contents 
##### Table of Contents  
1. [Reference Documentation](#reference_documentation)
2. [Terminology](#terminology)
3. [Pricing](#pricing)
4. [Setup](#setup)
5. [Details](#details)  
5. [Best Practices](#best_practices)  
6. [Exercise](#exercise)


<a name="reference_documentation"/>

# Reference Documentation
1. [Main Document](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-fleet.html)
   1. [Fleet request types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-fleet-request-type.html)
   2. 


 
<a name="terminology"/>

# Terminology

 - Fleet : Group of instances

<a name="details"/>

# Details
 

  - An EC2 Fleet contains the configuration information to launch a _fleet_—or _group—of_ instances. 
  - **In a single API call**, a fleet can launch 
    - multiple instance types 
    - across multiple Availability Zones, 
    - using the On-Demand Instance, Reserved Instance, and Spot Instance purchasing options together. 
  - Using EC2 Fleet, you can:
    - Define separate On-Demand and Spot capacity targets and the maximum amount you’re willing to pay per hour 
    - Specify the instance types that work best for your applications 
    - Specify how Amazon EC2 should distribute your fleet capacity within each purchasing option

![EC2 image](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/images/ec2-fleet.png)

## Request types

There are three types of EC2 Fleet requests: 
 - instant : EC2 Fleet places a synchronous one-time request for your desired capacity.
 - request : If you configure the request type as request, EC2 Fleet places an asynchronous one-time request for your desired capacity
 - maintain : If you configure the request type as maintain, EC2 Fleet places an asynchronous request for your desired capacity, and maintains capacity by automatically replenishing any interrupted Spot Instances. 
    

<a name="pricing"/>

# Pricing
 

<a name="setup"/>
  
#Setup

<a name="best_practices"/>

# Best Practices


<a name="exercise"/>

# Exercise

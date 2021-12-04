# Instance Types

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

1. [Main Documentation](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-types.html)
   1. [Instance Discovery](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/instance-discovery.html)
   2. [AWS Instance Types](https://aws.amazon.com/ec2/instance-types/)

<a name="details"/>

##Details

 - Each instance type offers different compute, memory, and storage capabilities 
 - It is grouped in an instance family based on these capabilities.
 - Types of Instances
   - General Purpose : General purpose instances provide a balance of compute, memory and networking resources 
   - Compute Optimized : Compute Optimized instances are ideal for compute bound applications that benefit from high performance processors. 
   - Memory Optimized : Memory optimized instances are designed to deliver fast performance for workloads that process large data sets in memory.
   - Accelerated Computing : Accelerated computing instances use hardware accelerators, or co-processors, to perform functions, such as floating point number calculations, graphics processing, or data pattern matching, more efficiently than is possible in software running on CPUs.
   - Storage Optimized : Storage optimized instances are designed for workloads that require high, sequential read and write access to very large data sets on local storage. They are optimized to deliver tens of thousands of low-latency, random I/O operations per second (IOPS) to applications.
 
### Instance Features

   - Burstable Performance Instances : T2/T3 series - Burstable Performance Instances provide a baseline level of CPU performance with the ability to burst above the baseline.
   - Fixed Performance Instances : M5, C5, and R5
   - CPU Credits : 
     - A CPU Credit provides the performance of a full CPU core for one minute.
     - T instances’ baseline performance and ability to burst are governed by CPU Credits.
     - T instances accrue CPU Credits when they are idle, and use CPU credits when they are active.
   
### Naming Conventions

 - Instance type names combine the instance family, generation, and size. They can also indicate additional capabilities, such as:
    - a – AMD processors 
    - g – AWS Graviton processors 
    - i – Intel processors 
    - d – Instance store volumes 
    - n – Network optimization 
    - b – Block storage optimization 
    - e – Extra storage or memory 
    - z – High frequency
    
 
<a name="terminology"/>

# Terminology

- Instance Family : Group of similar instance types based of a usage or other characteristics

<a name="pricing"/>

# Pricing


- If the instance needs to run at higher CPU utilization for a prolonged period, it can do so at a flat additional charge of **5 cents per vCPU-hour.**



<a name="setup"/>
  
#Setup

<a name="best_practices"/>

# Best Practices


<a name="exercise"/>

# Exercise

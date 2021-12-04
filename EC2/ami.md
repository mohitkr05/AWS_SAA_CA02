# Amazon Machine Images - AMI


# Table of Contents 
##### Table of Contents  
1. [Reference Documents](#reference-documentation)
2. [AMI Introduction](#ami-introduction)
3. [AMI Lifecycle](#ami_lifecylce)
4. [Exercise](#excercise)
   1. Create an Amazon EBS-backed Linux AMI
   2. Create an instance store-backed Linux AMI 


<a name="reference-documentation"/>

# Reference Documentation

1. [Main Documentation](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AMIs.html)
   1. [AMI Lifecycle](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ami-lifecycle.html)

<a name="ami-introduction"/>

# AMI Introduction


 - Provides information required to launch an instance.  
 - You must specify an AMI when you launch an instance
 - Can launch multiple instances from a single AMI
 - AMI Includes
   - One or more Amazon Elastic Block Store (Amazon EBS) snapshots
   - for instance-store-backed AMIs, a template for the root volume of the instance (for example, an operating system, an application server, and applications). 
   - Launch permissions that control which AWS accounts can use the AMI to launch instances. 
   - A block device mapping that specifies the volumes to attach to the instance when it's launched.




<a name="ami_lifecylce"/>

# AMI Lifecycle

 - The process of creating an AMI is called _register_
 - The process of removing an AMI is called _deregister_


![AMI Lifecycle -src AWS documentation](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/images/ami_lifecycle.png)

## Storing AMIs in S3 Bucket

- You can store an Amazon Machine Image (AMI) in an Amazon S3 bucket
- Copy the AMI to another S3 bucket, and then restore it from the S3 bucket. 
- By storing and restoring an AMI using S3 buckets, you can copy AMIs from one AWS partition to another, for example, from the main commercial partition to the AWS GovCloud (US) partition. 
- You can also make archival copies of AMIs by storing them in an S3 bucket. 
- The supported APIs for storing and restoring an AMI using S3 are 
  - _CreateStoreImageTask_ : Stores the AMI in an S3 bucket   
  - _DescribeStoreImageTasks_: Provides the progress of the AMI store task  
  - _CreateRestoreImageTask_: Restores the AMI from an S3 bucket 

# Pricing
 - Platform details : Example Redhat for Enterprise
 - Usage Operation : The run operation of an AMI example RunInstances:0010
   - Linux/UNIX 
     - RunInstances : Red Hat BYOL Linux
     - RunInstances:00g0 : Red Hat Enterprise Linux
     - RunInstances:0010 : Red Hat Enterprise Linux with HA
     


<a name="excercise"/>

# Exercise
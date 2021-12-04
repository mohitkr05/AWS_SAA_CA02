# Amazon EC2 - Amazon Elastic Compute Cloud 

1. [Main Documentation](https://docs.aws.amazon.com/ec2)
   1. [EC2 Linux](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/concepts.html)
   2. [EC2 Windows](https://docs.aws.amazon.com/AWSEC2/latest/WindowsGuide/concepts.html)
   3. [EC2 Nitro](https://docs.aws.amazon.com/enclaves/latest/user/nitro-enclave.html)
   4. [EC2 API Reference](https://docs.aws.amazon.com/AWSEC2/latest/APIReference/Welcome.html)
   5. [EC2 CLI Reference](https://docs.aws.amazon.com/cli/latest/reference/ec2/)
   6. [EC2 Instance connect](https://docs.aws.amazon.com/ec2-instance-connect/latest/APIReference/Welcome.html)
   7. [EC2 Auto scaling](https://docs.aws.amazon.com/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html)
   8. [VM Import/Export](https://docs.aws.amazon.com/vm-import/latest/userguide/what-is-vmimport.html)


# Table of Contents 
##### Table of Contents  
1. [Terminology](#terminology)
2. [Pricing](#pricing)
3. [Setup](#setup)
4. [EC2 Linux](#ec2_linux)  
5. [Exercise](#exercise)

<a name="terminology"/>

## Terminology
  
- Instances : Virtual Computing environments - Compare it to Virtual machines
- AMIs (Amazon Machine Images) : Images used to boot the virtual machines - Compare to snapshots or ova files
- Instance types : Configuration of CPUs, compare to flavours
- Key Pairs : SSH key pairs for accessing _Instances_ 
- Instance store volumes : Temporary data for your _Instances_ , deleted once the instance is stopped, hibernated or terminated
- Elastic Block storage : Persistent storage 
- Regions : Geographically located data centers
- Availability Zones : Redundant data center in the same _region_
- Tags : Metadata for Amazon resources
- VPCs (Virtual Private clouds)  - Virtual networks for logical isolation of resources.


<a name="pricing"/>

## Pricing

EC2 has the following purchase options

- On Demand Instances : Payment based on usage - Metric level is seconds(s) i.e. you are charged for number of seconds you use the resource
- Savings Plan : Long term based usage - 1 to 3 years, reduces the cost
- Reserved Instances : Reserve a specific virtual machine in a region - 1 to 3 years
- Spot Instances : Request unused EC2 instances
- Dedicated hosts : Pay for a physical host that is fully dedicated to running your instances, and bring your existing per-socket, per-core, or per-VM software licenses to reduce costs. 
- Capacity Reservations – Reserve capacity for your EC2 instances in a specific Availability Zone for any duration

<a name="setup"/>

## Setting up an EC2

1. (Create a key pair)[creating_key_pair.md] :  AWS uses public-key cryptography to secure the login information for your instance. A Linux instance has no password; you use a key pair to log in to your instance securely.  You cannot login to your instance untill or unless you have a key pair or you create an account and share the username and password
2. (Create a Security Group)[creating_security_group.md] : Security groups act as a firewall for associated instances and controls the inbound and outbound traffic. You cannot SSH untill the SSH port is open.
3. Other Information:
   1. The EC2 instance requires an EBS for the root directory. 
   2. You need to select the AMI and the instance type.
   3. You need to specify the Availability zone or AWS would automatically assign an AZ
   4. You attach the key pair at the time of launching the instance.
   5. You attach the instance behind the security group which helps in managing the incoming and outgoing traffic


![EC2 getting started (src AWS DOCS)](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/images/overview_getting_started.png)


## Instance Lifecycle

 - pending - The instance is preparing to enter the running state. An instance enters the pending state when it launches for the first time, or when it is started after being in the stopped state.  - No billing
 - running - The instance is running and ready for use - Not billed
 - stopping - The instance is preparing to be stopped or stop-hibernated. - Billed if preparing to hibernate
 - stopped - The instance is shut down and cannot be used. The instance can be started at any time.  - Not billed
 - shutting down- The instance is preparing to be terminated. - Not billed
 - terminated The instance has been permanently deleted and cannot be started. - Not billed
   - Reserved Instances that applied to terminated instances are billed until the end of their term according to their payment option.
   

### Operations
 - Launch  - When instance is launched it enters the _pending_ state
 - Stop and Start (EBS Backed instances only)
   - If instance fails check, or it is not responding, the instance can be _stopped_
   - Instance enters _stopping_ state and then _stopped_
   - You can modify instance settings in the _stopped_ state
   - When you start the instance it goes into the _pending_ state
   - The instance is moved to a new host computer
   - Instance retains it private IPv4 address
 - Hibernate (EBS Backed instances only)
   - Hibernate action signals OS to suspend to disk
   - It enters into the _stopping_ and then _stopped_ state
   - The instance is moved to a new host computer
   - Instance retains it private IPv4 address
 - Reboot
   - Recommended rebooting using the EC2 rather than system command
   - Rebooting an instance is equivalent to rebooting an operating system. 
 - Retirement
   - An instance is scheduled to be retired when AWS detects the irreparable failure of the underlying hardware hosting the instance
   - When an instance reaches its scheduled retirement date, it is stopped or terminated by AWS. 

![EC2 Instance lifecycle - src AWS Documentation](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/images/instance_lifecycle.png)

<a name="best_practices"/>

## Best Practices

- Best Practices
  - Manage access using IAM roles
  - Implement the least permissive role
  - Regularly patch update and secure operating system
- Storage
  - Use separate EBS volume for the OS and user data
  - Store temporary data in instance store
  - Encrypt EBS volumes and snapshots
- Resource management
  - Use Tags
  - Be aware of limits within EC2
- Backup and Recovery
  - Regular backup the EBS volumes using EBS Snapshots
  - Create AMIs for your instances
  - Deploy critical components across multiple AZs
  - Design application to use dynamic IP addressing to avoid failures 
  - Ensure to prepare for failure
  - Test the recovery procedures
- Networking
  - TTL should always be set to 255, there are chances it may expire for lower values
  

<a name="exercise"/>

## Exercise


 - Manage software on your Amazon Linux instance 
 - Manage user accounts on your Amazon Linux instance 
 - Processor state control for your EC2 instance 
 - I/O scheduler 
 - Set the time for your Linux instance 
 - Optimize CPU options 
 - Change the hostname of your Amazon Linux instance 
 - Set up dynamic DNS on Your Amazon Linux instance 
 - Run commands on your Linux instance at launch 
 - Instance metadata and user data

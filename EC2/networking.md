# Networking in EC2

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

1. [Main Document](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-networking.html)
   1. [Regions and Zones](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-regions-availability-zones.html)
   2. [EC2 Instance IP Addressing](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-instance-addressing.html#working-with-ip-addresses)
   3. [EC2 hostname types](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-naming.html)
   4. [BYOIP](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-byoip.html)
   5. [Assigning Prefixes](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-prefix-eni.html)
   6. [Elastic IP Addresses](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/elastic-ip-addresses-eip.html)
   7. [Elastic Network Interfaces](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-eni.html)
   8. [EC2 network bandwidth](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-network-bandwidth.html)
   9. [Enhanced networking](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/enhanced-networking.html)
   10. [Elastic Fiber adapter](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/efa.html)
   11. [Placement Groups](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/placement-groups.html)
   12. [MTU](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/network_mtu.html)
   13. [VPCs](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-vpc.html)
   14. [EC2-Classic](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-classic-platform.html)


<a name="terminology"/>

# Terminology

 - Amazon VPC  : Virtual Private cloud
 - Region : Geographically isolated collection of Data centers
 - Availability Zones : Multiple isolated data centers within each Region.
 - AWS Outposts :  brings native AWS services, infrastructure, and operating models to virtually any data center, co-location space, or on-premises facility.
 - Wavelength Zones :  allow developers to build applications that deliver ultra-low latencies to 5G devices and end users. 
  


<a name="details"/>

# Details
 
## Regions

Each Amazon EC2 Region is designed to be isolated from the other Amazon EC2 Regions
   - Some resources are tied to a region specifically
   - When you launch an instance, you must select an AMI that's in the same Region.
   - If the AMI is in another Region, you can copy the AMI to the Region you're using.


## Amazon VPC

- When you launch an instance, you can select a subnet from the VPC.
- The instance is configured with a primary network interface, which is a logical virtual network card.
- The instance receives a primary private IP address from the IPv4 address of the subnet, and it is assigned to the primary network interface. 
- By default, Amazon VPC uses the IPv4 addressing protocol
- When you create a VPC, you must specify an IPv4 CIDR block 
- You can optionally assign an IPv6 CIDR block to your VPC and assign IPv6 addresses from that block to instances in your subnets.

### VPC Subnets

- Private IP Addresses:
  - IPv4-only subnets: You can only create resources in these subnets with IPv4 addresses assigned to them. 
  - IPv6-only subnets: You can only create resources in these subnets with IPv6 addresses assigned to them. 
  - IPv4 and IPv6 subnets: You can create resources in these subnets with either IPv4 or IPv6 addresses assigned to them.
- Public IP Address:
  - Reachable from Internet
  - A public IP address is assigned to your instance from Amazon's pool of public IPv4 
  - If you require a persistent public IP address that can be associated to and from instances as you require, use an Elastic IP address instead.
  - **You can have multiple IP address associated with an Instance**
- Elastic IP address
  - An Elastic IP address is a public IPv4 address that you can allocate to your account. You can associate it to and disassociate it from instances as you require. It's allocated to your account until you choose to release it. 
  





<a name="pricing"/>


# Pricing
 

<a name="setup"/>
  
#Setup

<a name="best_practices"/>

# Best Practices


<a name="exercise"/>

# Exercise

 - Creating a VPC
 - Creating a subnet in a VPC
 - IPv6 and IPv4 addressing
 - Assigning multiple IPs to an Instance
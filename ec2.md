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
2. [EC2 Linux](#ec2_linux)  
3. [Emphasis](#emphasis)

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

<a name="ec2_linux"/>

## EC2 Linux


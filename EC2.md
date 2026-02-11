
# EC2 [Elastic Compute Cloud]
```
Amazon EC2 is a foundational service within the compute domain of AWS
It falls under IaaS
Using ec2 we can create virtual machine
virtualmachine / Instance / VM / server
EC2 is a region specific service
You can create 20 instances per region
```
## steps to create Instance *
```
1.Tag :

2.AMI [Amazon machine image]
AMI is a template which contains OS and other software which are required to launch your instance

3.Instance type :
It is nothing but combination of RAM & CPU

4.Security group
It is a virtual firewall which controls traffic of your instance

5.Storage : HDD or SSD

6.Key Pairs :
Key pairs are used to securely connect to your instance
 Types:
   1. Public key - kept with AWS
   2. Private key - Download by user
```
## Types of instance state:
```
Stop instance
Start instance
Reboot instance
Hibernate instance
Terminate instance
Running state
Pending state
```
Check status:
```
- Detect the problem that may appear
- Status check are basically Health checks
- 2/2 = all okay
- 1/2 = system is clear but instance not okay
  → To resolve this please reboot instance
- 0/2 = system and instance both are not okay
  → To resolve this please stop then restart instance
```




















































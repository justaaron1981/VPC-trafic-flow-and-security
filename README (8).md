<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# VPC Traffic Flow and Security

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-networks-security)

**Author:** Aaron  
**Email:** Justaaron1981@yahoo.com

---

## VPC Traffic Flow and Security

![Image](http://learn.nextwork.org/gleeful_red_proud_durian/uploads/aws-networks-security_92b0b0b4)

---

## Introducing Today's Project!

### What is Amazon VPC?

Allows users to create a logically isolated section within the AWS cloud, enabling them to define their own virtual network, similar to a traditional on-premises network, but with the scalability and flexibility of AWS.

### How I used Amazon VPC in this project

to create a logically isolated section of the AWS cloud where resources could be launched.

### One thing I didn't expect in this project was...

I didn't expect there to be a default ACL already connected to my subnet.

### This project took me...

120 minutes

---

## Route tables

Route tables are data structures that contain a set of rules, called routes, used to determine where network traffic should be directed.

Route tables are needed for making a subnet public because they define the rules for directing network traffic

![Image](http://learn.nextwork.org/gleeful_red_proud_durian/uploads/aws-networks-security_0a07b191)

---

## Route destination and target

'Routes are defined by their destination and target, which mean the destination specifies the network or IP address range to which the route applies. The target indicates where the traffic for that destination should be sent, such as a gateway, interface, or another network.

The route in my route table that directed internet-bound traffic to my internet gateway had a destination of 0.0.0.0/0 and a target of my VPC's internet gateway.


![Image](http://learn.nextwork.org/gleeful_red_proud_durian/uploads/aws-networks-security_0a07b191)

---

## Security groups

Security groups are collections of users, computers, or other groups that are used to manage access permissions to resources.

### Inbound vs Outbound rules

Inbound rules are firewall rules that control network traffic entering a network or device.

I configured an inbound rule that dictates what network traffic is allowed to enter a system or network.

Outbound rules are firewall rules that control network traffic originating from within a network and going out to external destinations like the internet or other networks

By default, my security group's outbound rule allows outbound traffic to all destinations



![Image](http://learn.nextwork.org/gleeful_red_proud_durian/uploads/aws-networks-security_92b0b0b4)

---

## Network ACLs

Network ACLs are sets of rules that control the flow of network traffic entering and leaving a subnet.

### Security groups vs. network ACLs

The primary difference between a security group and a network ACL is that security groups function as virtual firewalls for individual instances, controlling both inbound and outbound traffic, whereas network ACLs serve as a firewall for entire subnets, also controlling inbound and outbound traffic. 

---

## Default vs Custom Network ACLs

### Similar to security groups, network ACLs use inbound and outbound rules

By default, a network ACL's inbound and outbound rules will deny all traffic.

In contrast, a custom ACL's inbound and outbound rules are automatically set to deny all inbound and outbound traffic by default.

![Image](http://learn.nextwork.org/gleeful_red_proud_durian/uploads/aws-networks-security_4faeb056)

---

## Tracking VPC Resources

---

---

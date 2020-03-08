# Check AWS Security Group compliance
This project install a **CloudWatch Rule** and a **Lambda Function** to detect and remediate automatically any non compliant rule added in a **AWS Security Group**

## Prerequisite
As the **CloudWatch Rule** is fired on **CloudTrail** events, the **AWS Account** must have, at least, one enabled *Trail*

## Installation
Use **CloudFormation** to deploy a stack based on the *check-sg.yml* file

## Parameters
Parameters can be initiated in the **CloudFormation** stack and can be updated in the *Environment variables* of the **Lambda Function**
- **Flow** [rule_way] : Flow way = [ I ]ngress, [ E ]gress or [ A ]ll
- **IPv4** [rule_ip4] : Comma separated non compliant IPv4 CIDR masks
- **IPv6** [rule_ip6] : Comma separated non compliant IPv6 CIDR masks
- **Ports** [rule_ports] : Comma separated non compliant protocol ports

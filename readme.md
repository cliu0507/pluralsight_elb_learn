## ELB type
1. What is internet-facing type ELB?
2. What is  Internal-Only type ELB


# Internet Facing type ELB
## Health Check
ELB will health check each web server(back end server target)

## Available Zone
There can be multiple back end servers available in different zones (web1, web2)
ELB will have the intelligence to send to right zone


# Internal ELB
## Usage case
A set of web1 and web2 also connect with a ELB (internal) accessing some kinds of APIs, behind this ELB, there will a couple of EC2 instances running that web application needs

## How to architect?
You can have multiple layers of ELB

# Amazon ELB specs
## Example
The (internet-facing) ELB we use on AWS will automatically get a DNS name like:
<random>.us-east-1.elb.amazonaws.com  (DNS name)

## CNAME Alias
you can set up CNAME alias for <random>.us-east-1.elb.amazonaws.com so you can use your own domain name


## Application LB (level 7 HTTP, commonly used)
Commonly Used in real world production environment

## Network LB (level 4 TCP/IP)
Basically you can specify the traffic to specific ips

## Classic LB (legacy)
Legacy stuff that doesn't really need to memorize

# Website
https://app.pluralsight.com/library/courses/aws-load-balancing-implementing/table-of-contents

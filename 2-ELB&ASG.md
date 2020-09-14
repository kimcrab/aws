## AWS fundamentals
- Scalability means that an application / system can handle greater loads by adapting.
- High Availability means running your application / system in at least 2 data centers.
- Vertical Scaling: Increase instance size (= scale up)
- Horizontal Scaling: Increase number of instances (= scale out)

## ELB
- ELB provides Health Checks to know if EC2 instances are avaliable
- ELB has 3 Types
  - Classic Load Balancer(v1): HTTP, HTTPS, TCP
  - Application Load Balancer(v2): HTTP, HTTPS, WebSocket
  - Network Load Balancer(v2): TCP, TLS, UDP
- It is recommended to use the newer c2 generation.
- ELB access logs will log all access requests.
- CloudWatch Metrics will give you aggregate statistics.
- **ALB can route to multiple target groups.**
- Enabling stickiness may bring imbalance to the load over the backend.
- ALB provides Cross-Zone Load Balancing by default. (CLB&NLB don't)
- An SSL Certificate allows traffic between your clients and your load balancer to be encrypted in transit. (in-flight encrption)
- SSL refers to SEcure Sockets Layer, used to encrypt connections.
- TLS refers to Transport Layer Security, which is a newer version.
- Nowadays, TLS certificates are mainy used, but people still refer as SSL.

##ASG
- ASG is for scaling in/out to match traffic loads.
- ASG has following attributes
  - AMI + Instance Type / EC2 User Data / EBS Volumes / Security Groups / SSH Key Pair
  - Min Size / Max Size / Initial capacity
  - Network + Subnets Information
  - Load Balancer Information
  - Scaling Policies
- It is possible to scale an ASG based on CloudWatch alarms.
- But, it is better to define auto scaling rules that are directly managed by EC2.
- Use Launch Template (newer) prior to Launch Configuration. (legacy)

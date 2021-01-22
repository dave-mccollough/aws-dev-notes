## ELB - Elastic Load Balancer

### Links and Documentation
[OSI Model](https://en.wikipedia.org/wiki/OSI_model)
[AWS Docs](https://docs.aws.amazon.com/elasticloadbalancing/)


### Types of Load Balancers
- Application Load Balancers
- Network Load Balancers
- Classic Load Balancers

#### Application Load Balancers
- Best suited for balancing HTTP and HTTPS traffic
- Operates at Layer 7 
- Application Aware
- Supports advanced request routing - sends specific requests to specific web servers

#### Network Load Balancers
- Best suited for load balancing of TCP traffic - Extreme Performance
- Operates at layer 4
- Capable of handling millions of requests per second while maintaining ultra-low latency

#### Clasic Load Balancers
- Legacy load balancers
- Supports HTTP and HTTPS applications
- Supports Layer 7 features such as X-Forwarded and Sticky Sessions
- You can use strict Layer 4 load balancing fpr applications the rely purely on the TCP protocol
- If your application stops responding and returns a 504 error(Gateway timeout), that means the applicaton is having issues.  This could be at either the web server or database layer.  Identify issue and scale up/out as needed

#### X-Forwarded-For Header
- Users IP address appears in the X-Forwarded-For Header

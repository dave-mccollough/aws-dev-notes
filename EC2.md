## EC2 - Elastic Compute Cloud

### Pricing Options

#### On Demand
- Pay by the hour or second
- Most flexible option

#### Reserved 
- Reserve capacity for one or three years
- Up to 72% discount
- Reserved instances are regional
- Three Types of Reserved Instances
    - Standard Reserved Instances
        - Up to 72% 0ff on-demand pricing
        - Cannot change instance type
    
    - Convertible Reserved Instances
        - Up to 54% off on-demand pricing
        - Option to change to different instance type of equal or greater value

    - Scheduled Reserved Instances
        - Launched during time window specified
        - Schedule reservation for a window of time that suits you best

#### Spot 
- Set a maximum price you are willing to pay for the instance.  
- Price fluctuates with supply and demaand
- Purchase unused capacity at a discount of up to 90%
- Instance my be terminated or hibernated if price exceeds maximum bid price

#### Dedicated 
- Physical EC2 server dedicated for your use.
- Most expensive option
- Typically used for compliance requirements or licensing that does not support multi-tenancy or cloud deployments
- Can be purchased on-demand

#### AWS Savings Plans
- Save up to 72% regardless of instance type or region
- Commit to on or three years
- Includes other technologies such as Lambda and Fargate

#### AWS Pricing Calculator
- https://calculator.aws/#/

### EC2 Instance Types
- Each instance type offers different compute memory and storage capabilites
- Instance types are grouped into instance families

#### General Purpose Instances
- Good choice for most applications
- Small to medium databases or data processing tasks

#### Micro Instances
- Best suited for small applications or websites with low throughput

#### Compute Optimized Instances
- Higher ration of vCPU to memory
- Lowest cost per vCPU
- Best suited for Batch processing, web servers, applications requiring high performance

#### FPGA Instances
- Provide customizable field programmable gate arrays that can be programmed to created specific hardware accelerations
- High CPU performance, high network bandwidth, large memory
- Best suited for data analytics, video processing, financial computing

#### GPU Instances
- Best suited for 3D graphics, HPC, rendering and media processing

#### Machine Learning Instances
- Powered by chips custom built by AWS
- Optimized for machine learning applications, image and speech recognition and NLP

#### Memory Optimized
- Lowest cost per GB of RAM
- Best suited for Database Applications and memory intensive applications

#### Storage Optimized
- Best suited for applications with specific disk I/O requirements
- Recommended for NoSQL databases or data warehouses
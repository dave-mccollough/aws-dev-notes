## EBS - Elastic Block Store

### Documentation
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/AmazonEBS.html
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ebs-volume-types.html

### What is EBS
- Storage volumes (disks) you can attach to your EC2 instance 
- When you launch an EC2 instance, it has at least one EBS volume attached for the OS
- You can add more volumes as needed
- You can use EBS volumes as you would any system disk
  - File Systems
  - Databases
  - Applications

### EBS Features
- Designed for production workloads
- Highly Available
  - Automatically replicated within a single AZ to protect against hardware failures
- Scalable 
  - Dynamically increase capacity/change type with no downtime or performance degredation to live systems

### EBS Types

#### General Purpose SSD (gp2)
  - Balance of price and performance
  - 3 IOPS per GB, up to 16,0000 IOPS per volume
    - IOPS = Input/Output Operations per Second
  - gp2 volumes smaller than 1 TB can burst to 3,000 IOPS
  - Use Case:  Boot volumes or dev/test applications that aren't latency sensitive

#### Provisioned IOPS SSD (io1)
- 99.8% - 99.9% Durability
- High performance and most expensive
- Up to 64,000 IOPS per volumne, 50 IOPS per GB
  - Use if you need more than 16,000 IOPS
- Use Case:  
  - I/O intensive applications
  - Large databases
  - Latency sensitive workloads

#### Provisioned IOPS SSD (io2)
- 99.99% Durability
- 500 IOPS per GB, up to 64,000
- Latest generation of provisioned IOPS
- More durable and performant
- Same price as io1
- Use Case:  
  - I/O intensive applications
  - Large databases
  - Applications that need high levels of durability


#### Throughput Optimized HDD (st1)
- **Cannot be a boot volumne**
- HDD
- Lower cost
- Throughput of 40 MB/s per TB
- Able to burst to 250 MB/s per TB
- Maximum throughput of 500 MB/s per volume
- Use Case:  Storing large amounts of frequently accessed data
  - Big Data
  - Data Warehouse
  - ETL
  - Log Processing
- Cost effective way to store large volumes of data

#### Cold HDD SC1
- **Cannot be a boot volumne**
- HDD
- Lowest cost option
- Throuoghput of 12 MB/s per TB
- Able to burst to 80 MB/s per TB
- Use Case:  
  - Colder data that require fewer scans per day
  - Applications where performance is not a factor
  
### IOPS vs Throughput

#### IOPS
- Measures number of read/write operations per second
- Important metric for determining transaction speed
  - Low latency applications
  - Actions reads/writes very quickly
- If you need high IOPS, choose Provisioned IOPS SSD (io1/io2)

#### Throughput
- Measures number of bits read or written per second (MB/s)
- Important metric for complex queries
  - Large Datasets
  - Large I/O sizes
- If you need high throughput, choose Throughput Optimized HDD (st1)

### Other Notes
- EBS volume needs to be in the same AZ as the EC2 instance
- Volumes can be created based on Snapshots
  - Volumes created from encrypted snapshots are automcatically encrypted
  - Volumes created from unencrypted snapshots are automatically unencrypted
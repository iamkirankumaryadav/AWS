# **AWS**

### **Amazon Web Services**

AWS has myriad services for doing all kinds of things! While you don’t need to be familiar with them all, outlined below are a few that give you a sense of what type of services we provide and how they are billed. 

### General Services

1. **CodePipeline**
- This will build code and can deploy it to various AWS services. It is charged per pipeline. Can be used with Elastic Beanstalk for blue/green no-downtime deployments.

2. **Elastic Load Balancing**
- Distributes traffic across application servers, such as EC2, Lambda or Fargate. Can use health checks to know which servers should service requests. Charges are based on the number of hours the load balancer runs and (at a high level) the amount of traffic it services. The actual charging rules can be quite complex.

3. **RDS**
- Relational database hosting platform. Charged in the same way as EC2 (i.e. a virtual machine with a set amount of resources). Servers can be resized but must be restarted to do so.

4. **Route 53**
- AWS domain and DNS management.

5. **S3**
- Store objects in the cloud. Charged based on the amount of data being stored, how it’s stored, and for retrieval.

### **Application Executors**

AWS provides a few ways of executing applications, from virtual machines to container executors to function executors.

1. **EC2**
- Scalable virtual servers. Charged based on resources of the virtual servers (RAM, CPU, storage), per hour. Servers can change their resource allocation but must be restarted to apply them.

2. **Fargate**
- Run containerized applications (e.g., Docker images). Charges are based on the resources assigned to the container (RAM, CPU, etc.) and how long it runs. Very scalable but can require manual orchestration.

3. **Lambda**
- An application is uploaded to Lambda and only executed when triggered, for example, on an HTTP request or via S3. For example, a Lambda instance would run to just service a single HTTP request. Charging is based on the amount of memory the Lambda uses and how long it runs for, plus the number of requests. Sometimes data transfers can also be charged depending on which region(s) a Lambda is fetching data from. Highly scalable up and down. Not suited for serving static content.

4. **Lightsail**
- Virtual machines, like EC2 but simpler to set up. Charges are based on the resources of the Lightsail virtual machine. Virtual machines' resources can’t be changed, instead, the machines must be cloned to a new instance and restarted. 

5. **Elastic Beanstalk**
- Ties together EC2, RDS and Elastic Load Balancing with simple configuration and deployment. Its primary advantage is how it can facilitate the autoscaling of EC2 instances. Billing is based on a combination of the EC2, RDS and ELB that you use. Deployment is made easy with CLI tools, and we can use rolling deployments so there is no downtime. It has support for several languages including Python, NodeJS, Java and Go.

### **Availability Zones**

For extra redundancy, services can be deployed across multiple availability zones (AZ). This means that requests can fall over from one AZ to another in the case of infrastructure failure. In general, the cost of a service is multiplied by the number of availability zones it’s in.

You should be able to tell the customer why you have chosen Elastic Beanstalk what components it contains, and the purpose of these. The AWS resource pages for each service contain descriptions of how they are charged.

- CodePipeline
- Elastic Load Balancing
- RDS
- Route 53
- S3
- Elastic Beanstalk

The concrete pricing differs in each region, however, the method of the price calculation is the same. For example, an EC2 instance in Region A may cost more than the same instance in Region B, however, both are billed at an hourly rate. The AWS pricing calculator at https://calculator.aws/ can also give some guidance.

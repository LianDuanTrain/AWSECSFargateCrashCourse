<!-- How to Create an Application Load Balancer with AWS ECS Fargate -->

##  **Topics** 
- <h3>What is AWS Elastic Load Balancing?</h3> 
- <h3>Hands-on Demo Overview and Key Points</h3>
- <h3>Create an Application Load Balancer with AWS ECS Fargate</h3>   
- <h3>Verify Application Load Balancer and AWS ECS Fargate</h3> 
- <h3>Cleanup AWS Resources</h3> 


## **What is AWS Elastic Load Balancing?**
- <h3>Distributes incoming traffic across multiple targets, such as EC2 instances,containers, and IP addresses</h3>
- <h3>Load balancers</h3>    
   -  Application Load Balancer     
   -  Network Load Balancer     
   -  Gateway Load Balancer 
   

## **Hands-on Demo Overview and Key Points**
- <image src='./images/aws.jpg'  width="100%">


## **Create an Application Load Balancer with AWS ECS Fargate**

- Create an Application Load Balancer
  - Name is DemoFargateALB

- Create a New Security Group 
  - Name is DemoFargateALBSecurityGroup


- Create a Target Group
  - Name is DemoFargateALBTargetGroup
    - Choose a target type is IP addresses

- Create a Fargate Cluster
  - Name is DemoFargateCluster
    
- Create a Task Definition
  - Name is DemoAppTask
    - Container name is DemoApp
    - Container image is lianduantraining/react-app
    
- Create a Fargate Service 
   - Name is DemoService
   - Security group name is DemoServiceSecurityGroup

- Edit Security Group
   - DemoServiceSecurityGroup 
    - Edit Inbound rules


## **Verify Application Load Balancer and AWS ECS Fargate** 
- <h3>Access AWS ECS Fargate Service via ALB DNS Name</h3> 


## **Cleanup AWS Resources**
- <h3>Delete Service</h3>
- <h3>Delete Cluster</h3> 
- <h3>Delete ABL</h3> 
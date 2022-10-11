# How to Deploy Docker Container to AWS ECS Fargate?  

## Topics  
- How to Create an AWS ECS Fargate Admin User? 
- How to Create an AWS ECS Fargate Cluster?   
- How to Deploy Docker Container to AWS ECS Fargate?  
- Cleanup AWS Resources

## How to Create an AWS ECS Fargate Admin User? 
- Identity and Access Management (IAM)
- Select User
  - Add users
  - Permissions   
    - AmazonECSTaskExecutionRolePolicy
    - AmazonECS_FullAccess  
  - [<image src='./images/permissions.jpg'  width="50%">]
  - Check Role
    - ecsTaskExecutionRole
    - [Amazon ECS task execution IAM role](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/task_execution_IAM_role.html)
## How to Create an AWS ECS Fargate Cluster?    
- Elastic Container Service  
  - Select Clusters
  - Click Create Cluster  

## How to Deploy Docker Container to AWS ECS Fargate?   
### Task Definition 
  - Elastic Container Service  
    - Select Task Definitions
    - Create new a Task Definition
       - Container definitions 
       - [<image src='./images/container.jpg'  width="80%">]
### Run Task    
  - VPC and security groups  
  - [<image src='./images/vpc.jpg'  width="60%">]  
  - Security groups    
### Verify Container Access
  - Clusters
    - Tasks
      - find Public IP
      - curl IP:8080
## Cleanup AWS Resources  
- Stop Task 
- Delete Cluster

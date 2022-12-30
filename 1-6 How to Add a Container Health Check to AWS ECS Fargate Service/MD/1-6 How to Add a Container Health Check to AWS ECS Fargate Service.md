# **👨‍⚕️How to Add a Container Health Check <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; to AWS ECS Fargate Service？** 

## **📣What we will cover:**    
- **<h3>📑Why do We Need Health Check in Fargate Service?</h3>** 
   
- **<h3>🔎How to Add a Health Check to Fargate Service?</h3>**  
  
- **<h3>🖐️Hands-on Demo</h3>**   
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>   
<br>
<br>
<br>      
📌 

## **📑Why do We Need Health Check in Fargate Service?**
- **<h3>🔩Keep Desired  Number of Tasks in the REPLICA Service</h3>**
  
- **<h3>🛠️ECS Rolling Deployment</h3>** 
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>   
<br>
<br>
<br>      
📌 

## **🔎How to Add a Health Check to Fargate Service?**
- **<h3>🧾Pre-request</h3>**
  - Health Check API in Microservice
  - Health Check Command is Available on Docker Image 
  - Docker Container Pass Health Check
    - ```docker run --name=healthCheckTest -d  --health-cmd='curl -f http://localhost:9999/actuator/health/ping || exit 1'```
    - 📚[docker run --health-cmd,--health-interval,--health-retries,--health-start-period,--health-timeout](https://docs.docker.com/engine/reference/commandline/run/)


- **<h3>⚙️Configure Container Health Check in Task Definition</h3>** 
  - Health Check Command: ```CMD-SHELL,curl -f http://localhost:9999/actuator/health/ping || exit 1```
  - <div id="wrapper-div" style="box-shadow: 0px 2px 25px rgba(0, 0, 0, .25);  width:fit-content"  width="100%"><image src='./images/config.jpg'   width="400px"> </div>  
  -  📚[Amazon Elastic Container Service Health Check](https://docs.aws.amazon.com/AmazonECS/latest/APIReference/API_HealthCheck.html)


<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>   
<br>
<br>
<br>      
📌 

## **🖐️Hands-on Demo**
 
- **<h3>🎯Demo Goals</h3>**
  - Update a Task Definition with Health Check
  - Use the Task Definition to Create a Service      

- **<h3>🛑Cleanup AWS Resources</h3>** 
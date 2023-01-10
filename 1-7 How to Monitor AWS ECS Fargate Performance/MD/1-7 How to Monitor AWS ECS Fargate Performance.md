<!--# How to Monitor AWS ECS Fargate Performance? | CloudWatch Container Insights-->
📌
# **👨‍💻How to Monitor(and Analysis) AWS ECS Fargate Performance?**

## **📣What We Will Cover:**    
- **<h3>✒️Enable Container Insights to Monitor AWS ECS Fargate</h3>** 
   
- **<h3>✍️Hands-on Demo: Enable Container Insights in Fargate</h3>** 

- **<h3>✍️Hands-on Demo: Analysis of Fargate Performance in CloudWatch</h3>** 

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

## **✒️Enable Container Insights to Monitor AWS ECS Fargate** 
### **⭐New Fargate Cluster**
  - <div id="wrapper-div" style="box-shadow: 0px 2px 25px rgba(0, 0, 0, .25);  width:fit-content"  width="100%"><image src='./images/Insights.jpg'   width="600px"> </div> 

### **⚡️Existing Fargate Cluster**
```
aws ecs update-cluster-settings --cluster cluster_name_or_arn  --settings name=containerInsights,value=enabled --region us-east-2
```
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

## **✍️Hands-on Demo: Enable Container Insights in Fargate** 

- **<h3>🎯Demo Goals</h3>**
  
  - **<h3>Create an Application Load Balancer</h3>**


  - **<h3>Create a Fargate Cluster with Container Insights Enable</h3>**


  - **<h3>Create a Service</h3>**

  - **<h3>Run a Postman Collection to Call the Application Load Balancer</h3>**

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

## **✍️Hands-on Demo: Analysis of Fargate Performance in CloudWatch**

- **<h3>🎯Demo Goals</h3>**

  - **<h3>Run Load Testing with Postman Collection</h3>** 


  - **<h3>CloudWatch Overview</h3>**


  - **<h3>Container Insights</h3>**


  - **<h3>Logs Insights</h3>**


- **<h3>⚠️AWS Resource Cleanup</h3>**
  
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
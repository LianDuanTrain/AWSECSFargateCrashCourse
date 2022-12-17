 # **🎯How to Enable and Search <br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; AWS ECS Fargate Log?**     


## **📣What we will cover:**       
- **<h3>📑 AWS ECS Fargate Log Driver Types</h3>**      
  
- **<h3>🖐️Hands-on Demo - 🏃Run a Fargate Task and Check Log</h3>**
- **<h3>🖐️Hands-on Demo - 🔎How to Search AWS ECS Fargate Log in Cloudwatch?</h3>**

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

## **📑AWS ECS Fargate Log Driver Types**   

         
- **<h3>Log Driver Types</h3>**       
  - **<h3>awslogs(Default)</h3>**  
  - **<h3>splunk</h3>**  
  - **<h3>awsfirelens</h3>**  


- **<h3>Container Definitions</h3>**      

  - <div id="wrapper-div" style="box-shadow: 0px 2px 25px rgba(0, 0, 0, .25); "><image src='./images/logtypes.png'  width="100%"> </div>  

<br>
     
📌 

## **🏃Run a Fargate Task and Check Log**   
    
- **<h3>Create SpringbootDemoTask</h3>**
  - [How to Deploy Docker Container to AWS ECS Fargate?](https://youtu.be/B6qSLd0SZpU)
  - Docker Image: lianduantraining/springbootdemo:V10
  - Port Number is  9999  


- **<h3>Run a Postman's collection to access SpringbootDemo APIs</h3>**

- **<h3>Check Log in Task UI</h3>**        
  - <div id="wrapper-div" style="box-shadow: 0px 2px 25px rgba(0, 0, 0, .25); "><image src='./images/tasklog.png'  width="100%"> </div>
   
      
📌 

## **🔎How to Search AWS ECS Fargate Log in Cloudwatch?**   
   
-  **<h3>Logs Insights</h3>**     
    - <div id="wrapper-div" style="box-shadow: 0px 2px 25px rgba(0, 0, 0, .25);  width:fit-content"  width="100%"><image src='./images/logsearch.png'   width="400px"> </div>   
    - 📘[Using the awslogs log driver](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/using_awslogs.html)
    - 📘[Analyzing log data with CloudWatch Logs Insights](https://docs.aws.amazon.com/AmazonCloudWatch/latest/logs/AnalyzingLogData.html)      

- **<h3>💥AWS Resource Cleanup</h3>**  
📌
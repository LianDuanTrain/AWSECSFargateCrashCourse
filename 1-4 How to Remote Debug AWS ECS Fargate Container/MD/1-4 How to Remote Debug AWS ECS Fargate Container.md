# **🐞How to Remote Debug AWS ECS Fargate Container?**

##  **⛳What we'will cover:** 
- **<h3>✒️ How to Create an ECS Remote Debug Policy？</h3>**
- **<h3>✒️ How to Attach the Debug Policy to ECS Task Execution Role?</h3>**
- **<h3>✒️ Easy Add Linux Parameters in Target Task Definition</h3>**
- **<h3>✒️ How to Enable Remote Debug in Fargate Service Container?</h3>**  
- **<h3>✒️ How to Remote Debug Fargate Service Container in Local Dev Env?</h3>**
             
📌 

## **📃How to Create an ECS Remote Debug Policy？**
Policy Name: ECSRemoteDebug
  - <div id="wrapper-div" style="box-shadow: 0px 2px 25px rgba(0, 0, 0, .25); "><image src='./images/ECSRemoteDebug.png'  width="70%"> </div>
```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": [
                "ssmmessages:CreateControlChannel",
                "ssmmessages:CreateDataChannel",
                "ssmmessages:OpenControlChannel",
                "ssmmessages:OpenDataChannel"
            ],
            "Resource": "*"
        }
    ]
}
```
        
📌 

## **✏️How to Attach the Debug Policy to ECS Task Execution Role?**   
  - <div id="wrapper-div" style="box-shadow: 0px 2px 25px rgba(0, 0, 0, .25); "><image src='./images/addRole.jpg'  width="80%"> </div>
        
📌   

## **🎯Easy Add Linux Parameters in Target Task Definition** 
- Add Linux Parameters  
```
"linuxParameters": 
   {
     "initProcessEnabled": true
   },
```

- Use the  Task Definition to Create a Fargate Service
       
📌


## **📚How to Enable Remote Debug in Fargate Service Container?**  

- Update the Fargate Service
```  
aws ecs update-service  --region "us-east-1" --cluster "DemoFargateCluster" --service "DemoAppService" --task-definition "DemoAppTask:X"   --force-new-deployment  --enable-execute-command 
```
📘[AWS Document: update-service](https://awscli.amazonaws.com/v2/documentation/api/2.8.6/reference/ecs/update-service.html)

       
📌

## **🏆How to Remote Debug Fargate Service Container in Local Dev Env?**

### **Local Dev Env**  
- AWS CLI Version 
  - <image src='./images/cli.png'  width="100%">
  - AWS CLI Version 1: 1.22.3 or later 
  - AWS CLI Version 2: 2.3.6 or later
  - 📘[AWS Document: Installing or updating the latest version of the AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)
- Session Manager Plugin 
  - <image src='./images/sessionManagerPlugin.png'  width="100%"> 
  - 📘[AWS Document: Install the Session Manager plugin for the AWS CLI](https://docs.aws.amazon.com/systems-manager/latest/userguide/session-manager-working-with-install-plugin.html)

### **Run execute-command to Remote Debug Fargate Service Container** 

```
aws ecs execute-command --cluster DemoFargateCluster  --task 123b59686c3d47858a30d52f0b954b9d  --container DemoApp --interactive --command "/bin/sh"
```  
📘[AWS Document: execute-command](https://awscli.amazonaws.com/v2/documentation/api/2.8.6/reference/ecs/execute-command.html)






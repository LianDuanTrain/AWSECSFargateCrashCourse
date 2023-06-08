# **🥅 Push Docker Image to ECR Using AWS CLI**

## **🎯 Demo Goal**
  <div id="wrapper-div" style="box-shadow: 0px 2px 25px rgba(0, 0, 0, .25);  width:fit-content"  width="100%"><image src='./images/g.jpg'   width="800px"> </div>

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


## **🐾Hands-on Demo Steps:**

  - **<h3>📝Check Demo ENV</h3>**
  - **<h3>✍🏼Create an AWS Public ECR</h3>**
  - **<h3>🧑‍💻Create an AWS ECR Admin User</h3>**
  - **<h3>🏗️Build/Test Docker Image</h3>**
  - **<h3>🐳Docker Login to AWS ECR</h3>**
  - **<h3>🏋🏼Push Docker Image to AWS Public ECR</h3>**

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
<br>    
<br>     
<br> 
<br>
<br>
<br>
<br>       
📌


## **Check Demo ENV**

- `aws --version`
 - <div id="wrapper-div" style="box-shadow: 0px 2px 25px rgba(0, 0, 0, .25);  width:fit-content"  width="100%"><image src='./images/aws-cli-version.jpg'   width="800px"> </div>
- `docker version`
 - <div id="wrapper-div" style="box-shadow: 0px 2px 25px rgba(0, 0, 0, .25);  width:fit-content"  width="100%"><image src='./images/docker-version.jpg'   width="600px"> </div>
 
## **Create an AWS Public ECR**

 - <div id="wrapper-div" style="box-shadow: 0px 2px 25px rgba(0, 0, 0, .25);  width:fit-content"  width="100%"><image src='./images/ecr.jpg'   width="800px"> </div>
## **Create an AWS ECR Admin User**

 - <div id="wrapper-div" style="box-shadow: 0px 2px 25px rgba(0, 0, 0, .25);  width:fit-content"  width="100%"><image src='./images/ECRAdmin.jpg'   width="800px"> </div>
  
## **Build/Test Docker Image**

- Dockerfile  
```
FROM nginx:mainline-alpine3.17 
RUN echo '<h1>Hello, welcome to Terraform hands-on demo!</h1>' > /usr/share/nginx/html/index.html
```
- Build Docker Image
`docker build -t public.ecr.aws/q8h0q2b2/terraformdemo:v1 .` 

- Test Docker Image
`docker container run -d --rm -p 80:80 --name=mynginx public.ecr.aws/q8h0q2b2/terraformdemo:v1`  

## **Docker Login to AWS ECR**

-`aws ecr-public get-login-password --region us-east-1 | docker login --username AWS --password-stdin public.ecr.aws`


## **Push  Docker Image to  AWS Public ECR**

-`docker push public.ecr.aws/q8h0q2b2/terraformdemo:v1`









In case you are trying to pull images from a PUBLIC AWS repository, you must add the following user permissions to your policy:

{
"Version": "2012-10-17",
"Statement": [
    {
        "Effect": "Allow",
        "Action": [
            "ecr-public:GetAuthorizationToken",
            "sts:GetServiceBearerToken"
        ],
        "Resource": "*"
    }
 ]  
} 





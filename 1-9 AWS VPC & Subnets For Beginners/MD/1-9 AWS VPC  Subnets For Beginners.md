# **🥅 AWS VPC & Subnets for Beginners**

## **🎯 Demo Goal**
  - <div id="wrapper-div" style="box-shadow: 0px 2px 25px rgba(0, 0, 0, .25);  width:fit-content"  width="100%"><image src='./images/vpc.jpg'   width="800px"> </div>


## **📑 IPv4 CIDR Block Association Restrictions**
https://docs.aws.amazon.com/vpc/latest/userguide/configure-your-vpc.html

## **🗃️ EC2 User Data**

```
#!/bin/bash
yum update -y
yum install -y httpd
systemctl start httpd
systemctl enable httpd
INSTANCE_ID=$(curl -s curl http://169.254.169.254/latest/meta-data/instance-id)
INTERFACE=$(curl -s http://169.254.169.254/latest/meta-data/network/interfaces/macs/)
SUBNETID=$(curl -s http://169.254.169.254/latest/meta-data/network/interfaces/macs/${INTERFACE}/subnet-id)
HOST_NAME=$(curl -s curl curl http://169.254.169.254/latest/meta-data/hostname)
echo '<center><h1>This instance ID is INSTANCE_ID </h1></center><center><h1>This HostName is HOST_NAME </h1></center><center><h1>This instance is in the subnet with ID: SUBNETID </h1></center>' > /var/www/html/index.txt
sed -i "s/INSTANCE_ID/$INSTANCE_ID/" /var/www/html/index.txt
sed -i "s/HOST_NAME/$HOST_NAME/" /var/www/html/index.txt
sed "s/SUBNETID/$SUBNETID/" /var/www/html/index.txt > /var/www/html/index.html
```

## **⚠️Delete AWS Resource After You Exercise**



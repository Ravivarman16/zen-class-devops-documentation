# Project 7: Infrastructure Monitoring and Alerting with AWS CloudWatch

## 1.  Create an AWS EC2 instance and install a sample application that generates logs:

+ Create a new EC2 instance with the necessary security groups and key pairs.

+ Install a sample application that generates logs (e.g. Apache web server).

## 2.  Configure CloudWatch to monitor the logs and trigger alerts based on predefined metrics:

+ Create a new CloudWatch log group and specify the log stream from the sample application.

+ Define custom CloudWatch metrics based on the log data and set thresholds for alerting.

+ Configure CloudWatch alarms to trigger notifications (e.g. email, SMS) when the thresholds are breached.

## Test the monitoring and alerting by simulating a scenario that triggers the alert (e.g. overwhelming traffic to the application).

---


## **SOLUTION:**

## **Step:1 - Launching an EC2 instance:-**


### **1. Login into [AWS Management Console:](https://signin.aws.amazon.com/signin?redirect_uri=https%3A%2F%2Fconsole.aws.amazon.com%2Fconsole%2Fhome%3FhashArgs%3D%2523%26isauthcode%3Dtrue%26nc2%3Dh_ct%26src%3Dheader-signin%26state%3DhashArgsFromTB_eu-north-1_67569bb514fd7334&client_id=arn%3Aaws%3Asignin%3A%3A%3Aconsole%2Fcanvas&forceMobileApp=0&code_challenge=O-19Kk8URbYdcSReZJtf-59QKpGm4u3dALUVrpv1Fj4&code_challenge_method=SHA-256)**


![console](https://github.com/Ravivarman16/images/blob/main/Login%20into%20console.png)


---


### **2. Select the region, according to your preferences.**


![region](https://github.com/Ravivarman16/images/blob/main/region.png)


---


### **3. On the search panel search EC2, click that one:**


![EC2_SEARCH](https://github.com/Ravivarman16/images/blob/main/PROJECT-7/SEARCH_EC2.png)


---

### **4. Then EC2 Management console will appear, On that click launch instances:**


![Launch_instance](https://github.com/Ravivarman16/images/blob/main/PROJECT-7/LAUNCH_INSTANCE.png)


---


### **5. Then name the instance according to your preferences:**



![NAMING_INSTANCE](https://github.com/Ravivarman16/images/blob/main/PROJECT-7/NAMING_INSTANCE.png)



---


### **6. Then select AMI Image for the instance. Here you can choose AMI Image according to your preferences:**


![AMI_IMAGE](https://github.com/Ravivarman16/images/blob/main/PROJECT-7/AMI_IMAGE.png)


---


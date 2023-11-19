---

## **AWS EC2 AUTOSCALING**

![ALTER-ALB-MAIN](https://github.com/zen-class/zen-class-devops-documentation/assets/129171351/1a7d4696-1c75-48b6-adeb-5bbef322dd65)


__AWS EC2 Autoscaling__ helps you maintain application availability according to the demand by automatically adding or removing Amazon Elastic Compute Cloud (Amazon EC2) instances according to conditions that you define.

### **Example:**


![ALTER-EXAMPLE-ALB-EC2](https://github.com/zen-class/zen-class-devops-documentation/assets/129171351/7483a51d-67ad-4b32-94f3-65c88db8e6fb)



---


## Here are some key points about Amazon EC2 Autoscaling:

**1. Launch configuration & Launch template:** The launch configuration is the place where we set up all the details needed to create virtual machines through an **Autoscaling group.** This includes crucial information like the

+ **Amazon Machine Image (AMI)**


+ **Instance type**
+ **Security group settings**
+ **Key pair for secure access**
+ **Storage specifications**
+ **IAM roles for permissions**
+ **User data**

To simplify and replicate these settings easily, we create a **launch template.** This template captures the standardized configuration, ensuring that instances can be deployed consistently and at scale within the designated Autoscaling group.

---


**2. Amazon EC2 Autoscaling group:** is configured to manage the dynamic scaling of instances based on varying demands. It includes specifications on the number of instances to launch when there's a high load or demand, the minimum number of instances to maintain, and the desired number of instances for optimal performance. This setup allows for automatic adjustment of resources to ensure efficient and responsive scaling in response to changing conditions or requirements.


![autoscaling_group](https://github.com/zen-class/zen-class-devops-documentation/assets/129171351/95a76c2f-5c79-4f15-a830-356e15e78a79)



---


**3. Amazon EC2 Autoscaling Policy:** is a set of rules and instructions that govern the scaling behavior of an Autoscaling group in response to changing conditions. These policies define how the group should scale its capacity up or down based on criteria such as increased demand, decreased load, or other performance metrics.

+ **Scheduled Scaling**

+ **Dynamic Scaling:**

  + **Target tracking policy**


   + **Step scaling**
  + **Simple scaling**
+  **Predictive scaling**


![types of policies](https://github.com/zen-class/zen-class-devops-documentation/assets/129171351/76503764-7bfb-45d1-97c9-230b4f5bfe51)



---


## Types of Termination policies in AWS Ec2 Autoscaling:

Amazon EC2 Auto Scaling supports custom termination policies, they are
 
  +  **OldestInstance:** Selects the longest running instance.
 
  
  +  **NewestInstance:** Selects the shortest running instance.
  +  **OldestLaunchConfiguration:** Terminates the instance with the oldest configuration(default).
  +  **ClosestToNextInstanceHour:** Terminates the instance that is closest to the next billable hour(default).

---


## Ways to Work with Auto Scaling groups:

You can create, access, and manage your Auto Scaling groups using any of the following interfaces:
  
  +  **AWS Management Console:** 

  
  +  **AWS Command Line Interface (AWS CLI):** 
  +  **AWS Tools for Windows PowerShell:** 
  +  **AWS SDKs:** 
  +  **AWS CloudFormation:**


---

## Services that can integrated with Amazon EC2 Autoscaling:


Some of the services that be combined or integrated with Amazon EC2 Autoscaling are
  
  + **AWS ECS (Elastic Container Service)**
 
  
  + **AWS EKS (Elastic Kubernetes Service)**
  + **AWS EC2 (Elastic Compute Cloud)**
  + **AWS CloudWatch**



![integration](https://github.com/zen-class/zen-class-devops-documentation/assets/129171351/4bd94f77-6ebb-4863-845b-0bb83d164b3d)



---


## Amazon EC2 Auto Scaling benefits:
  
  + **Better fault tolerance:** Amazon EC2 Auto Scaling can detect when an instance is unhealthy, terminate it, and launch an instance to replace it.
  
  
  + **Better availability:** Amazon EC2 Auto Scaling helps ensure that your application always has the right amount of capacity to handle the current traffic demand.
  + **Better cost management:** Amazon EC2 Auto Scaling can dynamically increase and decrease capacity as needed. Because you pay for the EC2 instances you use, you save money by launching instances when they are needed and terminating them when they aren't.
  + **Distribute instances across Availability Zones:** If one Availability Zone becomes unavailable, Amazon EC2 Auto Scaling can launch instances in another one to compensate.

---


## Pricing for Amazon EC2 Auto Scaling:

+ There are no additional fees with Amazon EC2 Auto Scaling, so it's easy to try it out and see how it can benefit your AWS architecture. You only pay for the AWS resources (for example, EC2 instances, EBS volumes, and CloudWatch alarms) that you use.

+ To calculate the price use [AWS Pricing calculator](https://calculator.aws/#/).


---


## How to create AWS EC2 Autoscaling group:


### **1. Login into** [AWS Management Console:](https://signin.aws.amazon.com/signin?redirect_uri=https%3A%2F%2Fconsole.aws.amazon.com%2Fconsole%2Fhome%3FhashArgs%3D%2523%26isauthcode%3Dtrue%26nc2%3Dh_ct%26src%3Dheader-signin%26state%3DhashArgsFromTB_eu-north-1_67569bb514fd7334&client_id=arn%3Aaws%3Asignin%3A%3A%3Aconsole%2Fcanvas&forceMobileApp=0&code_challenge=O-19Kk8URbYdcSReZJtf-59QKpGm4u3dALUVrpv1Fj4&code_challenge_method=SHA-256)



![LOGIN_PAGE](https://github.com/zen-class/zen-class-devops-documentation/assets/129171351/3ea12109-c5fd-4485-8381-64a74ef6d555)



---


### **2. Select the region, according to your preferences.**


![region](https://github.com/zen-class/zen-class-devops-documentation/assets/129171351/58c8c795-f8e4-48f0-affd-ef125d6ac017)


---


### **3. Create an AMI Image.**


**Example Source:**


![SOURCE_WEB](https://github.com/zen-class/zen-class-devops-documentation/assets/129171351/5a9c4777-d4c7-4058-93e3-b59f8fec9983)



### To create an AMI Image, under instances click actions, then click image and templates, then click create image:



![AMI](https://github.com/zen-class/zen-class-devops-documentation/assets/129171351/fe5ed3d2-3acd-4ab1-9228-c31b9cc9a558)


---


### **4. Create Launch Template:**

### Under EC2 Console, left-side, click Launch template:



![launch template](https://github.com/zen-class/zen-class-devops-documentation/assets/129171351/9d295725-98ae-4c61-bd0d-3070ea2db880)



---


### **5. Create Target groups:**

### Under EC2 Management Console, Left-side, click target groups:



![Target group](https://github.com/zen-class/zen-class-devops-documentation/assets/129171351/15e544fb-b5fd-4a6a-999e-dd0125db6a15)



---


### **6. Create Load Balancer:**

### Under EC2 Management Console, Left-side, click Load balancers:



![Loadbalancer](https://github.com/zen-class/zen-class-devops-documentation/assets/129171351/1845f367-9ff6-4e0e-ac8f-7918aab69c48)



---


### **7. Create Amazon EC2 Autoscaling:**

### Under EC2 Management Console, Left-side, Click Auto Scaling Groups


![AUTOSCALING](https://github.com/zen-class/zen-class-devops-documentation/assets/129171351/cee574d9-5f79-4813-bf80-e23c8d448004)



### Click Create Autoscaling group, Then naming and selecting the launch template, click next:


![Naming the grouop ](https://github.com/zen-class/zen-class-devops-documentation/assets/129171351/d9f3237b-347d-4abc-9ba4-40f7a09345b3)



---


### Then select the VPC and subnet, click next:


![AUTOSCALING VPC](https://github.com/zen-class/zen-class-devops-documentation/assets/129171351/43c52473-3052-45fa-9587-fa51c9e3b710)



---

### Then select the Load Balancer and Target groups:


![SELECTING LOAD BALANCER](https://github.com/zen-class/zen-class-devops-documentation/assets/129171351/ca6b4de0-40bd-460e-821c-a5c853125ec6)



---

### Then select the health checks value according to your preference:



![Health checks](https://github.com/zen-class/zen-class-devops-documentation/assets/129171351/96760741-08a2-4f0d-8cb9-a5ffa6810d85)



---


### Then enter the desired, minimum and maximum value according to your preference:



![INSTANCE_VALUE](https://github.com/zen-class/zen-class-devops-documentation/assets/129171351/bc397dd1-6d34-4960-ade0-b18304bd41fd)



---


### Then select the scaling policies and enter the target value & instance warmup value:



![SCALING_POLICIES](https://github.com/zen-class/zen-class-devops-documentation/assets/129171351/ac524895-701c-46be-944d-943be344bdda)



---


### Adding notification (optional):



![AUTOSCALING_NOTIFICATION](https://github.com/zen-class/zen-class-devops-documentation/assets/129171351/55a90f53-d728-4926-b198-651e063d61fb)



---


### Adding tags:



![AUTOSCALING TAGS](https://github.com/zen-class/zen-class-devops-documentation/assets/129171351/0ccec844-c86a-43b0-a3da-8c573c7bdacd)



---


### Then review & Create, finally autoscaling groups will be created:


![AUTOSCALING_FINAL](https://github.com/zen-class/zen-class-devops-documentation/assets/129171351/412cfc19-3aca-4bb0-90b4-94a8124ce8b0)



---

### Autoscaling group working:


###  **Before:**


![BEFORE](https://github.com/zen-class/zen-class-devops-documentation/assets/129171351/e71e9b59-9e7f-4b26-bc2e-1a02b534455a)



---

### **Terminating the newly created instance:**


![TERMINATING](https://github.com/zen-class/zen-class-devops-documentation/assets/129171351/25b3ed0a-7441-48b1-9ba9-771fa2514f1b)


---

### **After:**


![TESTING_OUTPUT](https://github.com/zen-class/zen-class-devops-documentation/assets/129171351/dc0e8d67-a37b-49c3-aee2-97c0e008813e)



---


## Like to know more about AWS EC2 Autoscaling visit the [official website](https://aws.amazon.com/ec2/autoscaling/)

 

 





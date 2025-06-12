

#Problem : 
eliminating the need for infrastructure management often associated with Kubernetes. Running a cluster required redundant management nodes and over-provisioning due to slow autoscaling, leading to wasted resources. Scaling Issues: Managing high job volumes was challenging, more time is consumed on deployment. 


#Solution : 
AWS App Runner as an alternative to Kubernetes (K8s) for deploying web applications and APIs. App Runner offers a simplified, fully managed approach to container deployment, eliminating the need for infrastructure management often associated with K8s


steps: 

1. Create an App Runner service using github as source code

   ![image](https://github.com/user-attachments/assets/86933139-6bdb-49f5-9d28-dc507a1fade1)


2.Configure application build. 

Provide the following build settings:

Runtime – Choose Python 3.

Build command – Enter pip install -r requirements.txt.

Start command – Enter python server.py.

Port – Enter 8080.

![image](https://github.com/user-attachments/assets/bf3e8292-8664-42df-b995-df48e3445f0c)


3. Configure your service.

Under Environment variables, select Add environment variable. Provide the following values for the environment variable.

Source – Choose Plain text

Environment variable name – NAME

Environment value as any value 

![image](https://github.com/user-attachments/assets/8fac4f77-5799-4204-8f18-d494e476ca16)


4.Review and create page, verify all the details you've entered

5.Verify that your service is running.

![image](https://github.com/user-attachments/assets/4fce8579-78b9-4b53-ad97-18667e9623f5)

![image](https://github.com/user-attachments/assets/1600cc33-2c82-4a76-a8b2-7d8e0a980053)

6. Change your service code

 make a change to your code in the repository source directory. The App Runner CI/CD capability automatically builds and deploys the change to your service.

![image](https://github.com/user-attachments/assets/8a3bcfef-3523-4d5f-95c2-fd62b8184f98)


7. debug and troubeshoot

   we can see  logs for your service, attached to our app, there are 3 types of logs


   Event log – Activity in the lifecycle of your App Runner service. The console displays the latest events.

   Deployment logs – Source repository deployments to your App Runner service. The console displays a separate log stream for each deployment.

   Application logs – The output of the web application that's deployed to your App Runner service. The console combines the output from all running instances into a single log stream.

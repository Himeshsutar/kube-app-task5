🚀 TASK 5: Build a Kubernetes Cluster Locally with Minikube

✅ Objective

Deploy and manage applications in a Kubernetes cluster built using Minikube. Scale, expose, and troubleshoot apps using kubectl commands, YAML configuration files, and Kubernetes best practices.

🛠️ Tools & Technologies

Minikube

kubectl

Docker

YAML

📁 Project Structure

README.md – Documentation of steps performed and project details.

deployment.yaml – Kubernetes deployment configuration.

service.yaml – Kubernetes service configuration for app exposure.

Task5.md (optional) – Documentation for the individual steps of Task 5.

Pod logs and Kubernetes state – Generated during the task for troubleshooting.


🔧 Steps Performed

🔹 a. Install and Start Minikube Cluster

Installed Minikube and started the cluster using the following command:

minikube start

Verify the cluster status:

minikube status

🔹 b. Create Deployment

Created a deployment.yaml to define the app's deployment configuration.

Applied the deployment using:

kubectl apply -f deployment.yaml

🔹 c. Expose the Application

Created a service.yaml to expose the application using a Kubernetes Service.

Applied the service using:

kubectl apply -f service.yaml

Verify the service exposure:

kubectl get services

Accessed the app through Minikube:

minikube service nginx-server

🔹 d. Scale the Deployment  

Scaled the nginx-server deployment by adjusting the number of replicas using:

kubectl scale deployment nginx-server --replicas=3

Verify the scaled deployment:

kubectl get pods

🔹 e. Monitor and Troubleshoot Pods

Used kubectl describe to get detailed information about the pod's status and issues:

kubectl describe pod <pod-name>

View the logs of a pod using:

kubectl logs <pod-name>

🔹 f. Scale and Document Tasks

Scaled the application to the desired number of replicas and verified using kubectl get pods.

All actions and steps were documented in README.md and Task5.md.

✅ Result

1. Cluster Setup & Deployment

Screenshot: Cluster is successfully set up and the app is deployed in Minikube.

2. Service Exposure

Screenshot: The app is successfully exposed using a Kubernetes service.

3. Scaled Deployment

Screenshot: The app has been scaled with multiple replicas running.

4. Monitoring & Troubleshooting

Screenshot: Logs are being monitored and pod details are described for troubleshooting.

5. Final Review

Screenshot: Versioning and scaling tasks are completed successfully.

Successfully built a Kubernetes cluster locally with Minikube, deploying and scaling applications while utilizing kubectl to manage the resources. The workflow includes deployment, scaling, exposing the app with services, and troubleshooting.

📎 Notes

Minikube is used to simulate a local Kubernetes environment, perfect for testing and development purposes.

Always verify your pod and service status with kubectl get pods and kubectl get services.

When scaling, ensure the replicas are properly created and healthy by checking kubectl get pods and kubectl describe.

Tags are not needed for this task as it's more about cluster management and scaling.

Use kubectl describe for troubleshooting and analyzing pod details in case of issues (e.g., ImagePullBackOff).
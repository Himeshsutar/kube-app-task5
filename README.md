# TASK 5: Build a Kubernetes Cluster Locally with Minikube

## ✅ Objective

Deploy and manage applications in a Kubernetes cluster built using Minikube. Scale, expose, and troubleshoot apps using `kubectl` commands, YAML configuration files, and Kubernetes best practices.

## 🛠️ Tools & Technologies

* Minikube

* kubectl

* Docker

* YAML

## 📁 Project Structure

* `README.md` – Documentation of steps performed and project details.

* `deployment.yaml` – Kubernetes deployment configuration.

* `service.yaml` – Kubernetes service configuration for app exposure.

* `Task5.md` (optional) – Documentation for the individual steps of Task 5.

* Pod logs and Kubernetes state – Generated during the task for troubleshooting.


## 🔧 Steps Performed

**a. Install and Start Minikube Cluster**

Installed Minikube and started the cluster using the following command:

`minikube start`

Verified the cluster status:

`minikube status`

**b. Create Deployment**

Created a `deployment.yaml` to define the app's deployment configuration.

Applied the deployment using:

`kubectl apply -f deployment.yaml`

**c. Expose the Application**

Created a `service.yaml` to expose the application using a Kubernetes Service.

Applied the service using:

`kubectl apply -f service.yaml`

Verified the service exposure:

`kubectl get services`

Accessed the app through Minikube:

`minikube service nginx-server`

*Note: Replace 'nginx-server' with the actual name of your service if different.*

**d. Scale the Deployment**

Scaled the `nginx-server` deployment by adjusting the number of replicas using:

`kubectl scale deployment nginx-server --replicas=3`

*Note: Replace 'nginx-server' with the actual name of your deployment if different.*

Verified the scaled deployment:

`kubectl get pods`

**e. Monitor and Troubleshoot Pods**


Used `kubectl describe` to get detailed information about a pod's status and issues:

`kubectl describe pod <pod-name>`

*Replace <pod-name> with the specific pod you want to inspect.*

Viewed the logs of a pod using:

`kubectl logs <pod-name>`

*Replace <pod-name> with the specific pod whose logs you want to view.*

**f. Scale and Document Tasks**

Scaled the application to the desired number of replicas (e.g., 3 as shown in step d) and verified using:

`kubectl get pods`

All actions and steps were documented in `README.md` and optionally `Task5.md`.

## ✅ Result

* **Cluster Setup & Deployment:**
    ![setup and deploy](https://github.com/user-attachments/assets/3eb23d49-6930-4f14-9e47-682b98d02b44)

* **Service Exposure:**
    * *Screenshot showing:* The app is successfully exposed using a Kubernetes service.
* **Scaled Deployment:**
    * *Screenshot showing:* The app has been scaled with multiple replicas running.
* **Monitoring & Troubleshooting:**
    * *Screenshot showing:* Logs are being monitored and pod details are described for troubleshooting.
* **Final Review:**
    * *Screenshot showing:* Versioning and scaling tasks are completed successfully.

Successfully built a Kubernetes cluster locally with Minikube, deploying and scaling applications while utilizing `kubectl` to manage the resources. The workflow includes deployment, scaling, exposing the app with services, and troubleshooting.

## 📎 Notes

* Minikube is used to simulate a local Kubernetes environment, perfect for testing and development purposes.

* Always verify your pod and service status with:

    `kubectl get pods`

    `kubectl get services`

* When scaling, ensure the replicas are properly created and healthy by checking:

    `kubectl get pods`

    `kubectl describe deployment <deployment-name>`

    *Example: `kubectl describe deployment nginx-server`*

* Tags are not needed for this task as it's more about cluster management and scaling.

* Use `kubectl describe pod <pod-name>` for troubleshooting and analyzing pod details in case of issues (e.g., ImagePullBackOff, CrashLoopBackOff).

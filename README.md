# K8S 101 Challenge

This is a series of exercices and hands on in order to get into Kubernetes and start working on NGINX Ingress Controller.

## Capture the Flag
Of course, if there is a challenge, there will be a winner (I did not mention anything about a price though)!
Please go create a user account on [Capture the K8S Flag](http://ctfd.f5demolabs.org) and start playing.

But we will never leave you alone:
	- cheat-sheet:
	- flow diagram: 

For every lab you will find a series of questions that will give you coins. You can ask for hints in exchange of some coins.

---

## Lab0 - Getting familiar with your K8S Cluster
### Description
> Understanding the main components of a K8S Clutser, node types, basic networking, meaning and relationship between Services, Endpoints and Pods.

    **Useful commands**:
    kubectl cluster-info
    kubectl get nodes
    kubectl get namespaces
    kubectl get service -n *namespace*
    kubectl get endpoints -n *namespace*
    kubectl get pods -n *namespace*

---

## Lab1 - Build and deploy your first application
### Description
	- what is Container and why container registries are important?
	- managing secrets
	- to git, I git, git
	- deploy your application

> **Useful commands**:
>
>kubectl create secret docker-registry regcred --docker-server=<registry.gitlab.com> --docker-username=<your@email.addr> --docker-password=<yourpassword> -n <namespace>
>

---


## Lab2 - Make application accessible from outside
### Description:
	- Expose your application
	- Find the instructor container registry Deploy Token Username and Password
	- Deploy the ingress controller and create the Ingress Resource

**Useful commands**:
'''
kubectl port-forward deployment/webapp 5000:80
kubectl port-forward pods/webapp-867RY3R36R36 5000:80
kubectl port-forward service/webapp-svc 5000:webapp
'''

## Lab3 - Manage versioning of your application with Ingress
### Description
	- Deploy the version 2 (v2) of the web application
	- Deployment Strategies (Canary Realease, A/B Testing...)
	
You have multiple example you can inspire from at: https://github.com/nginxinc/kubernetes-ingress/tree/master/examples-of-custom-resources

**Useful commands**:
'''
'''

## Lab4 - East-West or Microservice-to-Microservice traffic
### Description
	- Deploy backend service
	- access your application and capture the flag!!!

**Useful commands**:
'''
'''


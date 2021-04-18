# Screenshots
To help review your infrastructure, please include the following screenshots in this directory::

## Deployment Pipeline
* DockerHub showing containers that you have pushed
* GitHub repository’s settings showing your Travis webhook (can be found in Settings - Webhook)
* Travis CI showing a successful build and deploy job

## Kubernetes
* To verify Kubernetes pods are deployed properly
```bash
kubectl get pods
```
![kubectl get pods](kubectlGetPods.png)

* To verify Kubernetes services are properly set up
```bash
kubectl describe services
```
![kubectl describe services](kubectlDescribeSerivces.png)

* To verify that you have horizontal scaling set against CPU usage
```bash
kubectl describe hpa
```
![kubectl describe hpa](kubectlDescribeHpa.png)


* To verify that you have set up logging with a backend application
```bash
kubectl logs {pod_name}
```
![kubectl logs](kubectlLogsUsers.png)
![kubectl logs](kubectlLogsUsers.png)


* Reverse proxy service
![Reverse Proxy Service](reverseProxyService.png)


* Travis CI build
![Travis-Ci Build](travisCiBuild.png)

* Docker Images in DockerHub
![DockerHub With Images](dockerHubWithImages.png)
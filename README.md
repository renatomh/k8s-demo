<h1 align="center"><img alt="K8s Demo" title="K8s Demo" src=".github/logo.png" width="250" /></h1>

# K8s Demo

## 💡 Project's Idea

This project was developed to practice deploying web applications with Kubernetes.

## 🛠 Technologies

During the development of this project, the following techologies were used:

- [Kubernetes](https://kubernetes.io/pt-br/)
- [minikube](https://minikube.sigs.k8s.io/docs/)
- [Docker](https://www.docker.com/)
- [MongoDB](https://www.mongodb.com/)
- [Node.js](https://nodejs.org/en/)

## 💻 Project Configuration

### First, you must install [Docker](https://www.docker.com/products/docker-desktop/) and [minikube](https://minikube.sigs.k8s.io/docs/start/) on your machine.

## 🕸 Kubernetes

Here's a list of useful commands for minikube and the Kubernetes CLI (kubectl):

### minikube

```bash
$ minikube start --driver docker # Pulls image and creates container for minikube with Docker
$ minikube status # Checks the minikube cluster status
$ minikube ip # Shows current minikube IP address
$ minikube stop # Stops the minikube cluster
$ minikube service webapp-service # Runs the webapp service when minikube IP is not accessible (it's a known issue)
```

### kubectl

```bash
$ kubectl get node # Shows current nodes
$ kubectl apply -f <config.yaml> # Applies a configuration (.yaml) file for cluster
$ kubectl get pod # Shows current cluster Pods
$ kubectl get svc # Shows current cluster services
$ kubectl get all # Shows all cluster components
$ kubectl get configmap # Shows cluster config maps
$ kubectl get secret # Shows cluster secrets
$ kubectl describe service <service-name> # Shows details about the service
$ kubectl describe pod <pod-name> # Shows details about the pod
$ kubectl logs <pod-name> # Shows logs for the pod/container (we can stream the logs with the -f option at the end of the command)
```

## ⏯️ Running

To deploy the application in a development environment, execute the following command on the root directory.

```bash
$ kubectl apply -f mongo-config.yaml
$ kubectl apply -f mongo-secret.yaml
$ kubectl apply -f mongo.yaml
$ kubectl apply -f webapp.yaml
```

### Documentation:
* [Kubernetes Crash Course for Absolute Beginners [NEW]](https://www.youtube.com/watch?v=s_o8dwzRlu4&t=275s)
* [minikube start](https://minikube.sigs.k8s.io/docs/start/)
* [Kubernetes Documentation](https://kubernetes.io/docs/home/)
* [developing-with-docker](https://gitlab.com/nanuchi/developing-with-docker/-/tree/feature/k8s-in-hour/)

## 📄 License

This project is under the **MIT** license. For more information, access [LICENSE](./LICENSE).

<p align="center">
  <a href="" rel="noopener">
 <img width=200px height=200px src="https://cdn.iconscout.com/icon/free/png-512/nodejs-2-226035.png" alt="Project logo"></a>
</p>

<h3 align="center">wapparticle41</h3>

<div align="center">

[![Status](https://img.shields.io/badge/status-active-green)]()
[![GitHub Issues](https://img.shields.io/github/issues/TitoFigueroa/wapparticle41-infra)]()
[![GitHub Pull Requests](https://img.shields.io/github/issues-pr/TitoFigueroa/wapparticle41-infra)]()
[![License](https://img.shields.io/github/license/TitoFigueroa/wapparticle41-infra)](/LICENSE)

</div>

---

## 📝 Table of Contents

- [About](#about)
- [Getting Started](#getting_started)
- [Deploy to k8s](#deployment)
- [ Deploy AWS Cloudformation Stacks](#aws_stacks)
- [Built Using](#built_using)
- [Authors](#authors)
- [Acknowledgments](#acknowledgement)

## 🧐 About <a name = "about"></a>

Wapparticle41 infrastructure repo contains all what we need to deploy this resource on a kubernetes cluster, and even the cluster stack to deploy in AWS.

The Kubernetes cluster contains the deployment of the containers with 3 pod replicas, and a service that allows expose the container using the cluster ip:port(8080), this routing is based on the label that we declared to the containers)

## 🏁 Getting Started <a name = "getting_started"></a>

### Prerequisites

- AWS accounts with permissions (this will allow your user to do the deployment using the cft)
- AWS Already created KeyPairs with the name "wappraticle41-keypair"
- Kubernetes (used to deploy the manifest of the app)

In case you dont have any of this please review links below that could help to install this prerequisites on your local environment

```
https://k3s.io/ --> a light weight Linux kubernetes version to install on your locall 
```

## Deploy to k8s

In order to spin up the app inside a kubernetes cluster you must execute the next command:

###  Files under "/deployment" folder

```
kubectl apply -f https://raw.githubusercontent.com/TitoFigueroa/wapparticle41-infra/main/deployment/k8s-deploy/wapparticle-deploy-k8s.yml
```

## Deploy AWS Cloudformation Stacks

Login into aws console, go to cloudformation stacks and create new one, follow next steps:

### Files under "/infrastructure" folder

```
VPC STACK CREATION ()
1) Create a stack uploading the template on the "Template is ready" option
2) Next stage will ask for a stack name, thats something you can handle
3) This step requires pass a parameter of environment, write "dev" please (for testing purpose)
4) Click Next, until you get deploy stack
5) See how the stack is created succesfully ;) 
```

```
K8S CLUSTER STACK CREATION
1) Create a stack uploading the template on the "Template is ready" option
2) Next stage will ask for a stack name, thats something you can handle
3) Click Next, until you get deploy stack
4) See how the stack is created succesfully ;) 
```

## ⛏️ Built Using <a name = "built_using"></a>

- [Kubernetes](https://kubernetes.io/) - Cluster Pod Orchestrator
- [Express](https://expressjs.com/) - Server Framework
- [AWS](https://aws.amazon.com/) - Cloud Provider

## ✍️ Authors <a name = "authors"></a>

- [@TitoFigueroa](https://github.com/TitoFigueroa)


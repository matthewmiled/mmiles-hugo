---
title: "Creating a CI/CD workflow with GitHub actions and AWS"
date: 2022-09-09
draft: false
categories: ["Tech"]
---

> Automating the process of building applications into docker images and deploying to a cluster.

### How do applications that are developed locally run in production?

- They need to be built into images
- The images need to be pushed to an image repository in the cloud
- The images need to be built into a container that can run on a virtual machine or pod in the cloud

### What tools can allow this?

- Docker can be used to build a python application into an image (via the steps set out in the Dockerfile)
- AWS has an Elastic Container Registry that can store docker images.
- Images can be built into containers.
- Kubernetes is a container orchestration tool that allows pods to run these images/apps (via containers). The Kubernetes cluster is set up in the cloud, and can be managed by AWS - Elastic Kubernetes Service. 
- AWS also offers Elastic Container Service to run containers in the cloud. 

### Using GitHub actions to automate this process

- The steps above can be carried out by writing commands in the terminal locally (e.g. running `docker build .` builds the app into an image)

- But GitHub actions also allows a virtual machine to run them whenever you push changes to a repo. 

- All of the commands and configuration are written in .yml files in the repo.

- I have created a couple of template Git projects that can automatically execute the process described above (the python application is very simple and just prints a statement). But it illustrates how production grade applications can be managed. 

- Any future projects I work on that need to run in production will be deployed via this process. 

- There is one project template for [deploying to Kubernetes via EKS](https://github.com/matthewmiled/python_app_to_k8s_automated).
However, using Kuberntes is slightly overkill for deploying small applications (especially those that just run on a cron schedule), so I have also created a version that [deploys the application to ECS](https://github.com/matthewmiled/python_app_to_ecs_automated). 

- The GitHub READMEs have a lot more information about the steps (see links above). 


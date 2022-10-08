---
title: Deploying a Django Web App to AWS Elastic Beanstalk
date: 2022-05-20
draft: false
categories: ["Tech"]
---

> An experiment with an AWS service to host a Django app.

In general, these are the key things that I wanted to achieve in order to say that a web app has been ‘deployed’:

- Support the use of a custom domain name.

- Support the use of HTTPS via SSL certificate.

- Auto redirect to HTTPS when there is any incoming traffic.

- Support the upload of images and ‘articles’ in django admin.

The source code for a template Django project is on my GitHub [(linked here)](https://github.com/matthewmiled/django-aws-eb-cookie-cutter). There are instructions included in the repo README on how to set up Elastic Beanstalk and configure the project.


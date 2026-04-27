PROJECT\_BRIEF.md

\# Project Brief — Lab Starter Application

\#\# Overview

Build a simple starter application repository for a cloud and DevOps lab.

This repository will be the starting point for the project The purpose of the project is to:

\- take an existing simple application  
\- understand how it works  
\- make small required modifications  
\- containerize it  
\- deploy it to the cloud using Infrastructure as Code

The starter application is  therefore a  simple, clean, easy to understand, and easy to run locally.


The application itself should be cloud-neutral which can be adapted and deployed differently depending on  cloud platform.

\---

\#\# What is expected from the Engineer

\- clone the repo  
\- run the application locally  
\- modify the application so the UI displays:  
  \- their full name  
  \- their cloud platform  
  \- environment  
  \- version  
  \- status  
\- make those displayed values come from environment variables  
\- containerize the application with Docker  
\- push the container image to a registry  
\- deploy it using IaC

This means the repo has already provided:

\- a working simple web application  
\- a health endpoint  
\- a very clear project structure  
\- clear local run instructions  
\- an easy place for interns to make the required changes

\---

\#\# Core requirements for the application

Build a very small web application with the following behavior.

\#\#\# Homepage  
The \`/\` route should return a simple but neat HTML page.

The page should clearly display these fields:

\- App Name  
\-Engineer Name  
\- Cloud Platform  
\- Environment  
\- Version  
\- Status

At starter state, the page can use placeholder values such as:

\- App Name: Cloud Lab Starter App  
\- Engineer Name: Replace Me  
\- Cloud Platform: Replace Me  
\- Environment: dev  
\- Version: v1.0.0  
\- Status: healthy

Important:  
\- these values should come from environment variables  
\- if an environment variable is not provided, the app can fall back to default placeholder values

\#\#\# Health endpoint  
The \`/health\` route should return a success response.

This can be JSON such as:

\- status: healthy

It should be simple and reliable.

\---

\#\# Technical direction

Use a stack that is simple and easy to understand.

Recommended stack:  
\- Python  
\- FastAPI  
\- Uvicorn

Why:  
\- simple  
\- lightweight  
\- easy Docker support  
\- easy to add environment variable handling  
\- easy to expose endpoints

Do not overengineer it.

\---

\#\# Project structure

Create a clean structure similar to this:

\`\`\`text  
lab1-starter-app/  
  app/  
    main.py  
    templates/  
      index.html  
    static/  
      style.css  
  requirements.txt  
  Dockerfile  
  .dockerignore  
  .gitignore  
  README.md

Notes:

* keep the structure small

* only add folders that are necessary

* do not add unnecessary frameworks or files

---

## **Application behavior details**

### **/**

* should render an HTML page

* should show the six visible fields clearly

* should look decent enough in a browser

* should not be plain unformatted raw text

* use a simple HTML template and a small CSS file

* styling should be minimal and clean

### **/health**

* should return a JSON response

* should be suitable for load balancer or ingress health checks later

* should return HTTP 200

---

## **Environment variables**

Support the following environment variables:

* APP\_NAME

* ENGINEER\_NAME

* CLOUD\_PLATFORM

* ENVIRONMENT

* APP\_VERSION

* APP\_STATUS

Default values can be:

* APP\_NAME=Cloud Lab Starter App

* ENGINEER\_NAME=Replace Me

* CLOUD\_PLATFORM=Replace Me

* ENVIRONMENT=dev

* APP\_VERSION=v1.0.0

* APP\_STATUS=healthy

The application should read these values at runtime and display them on the page.

---

## **Docker requirements**

Include a working Dockerfile.

The Dockerfile should:

* use a simple Python base image

* install dependencies from requirements.txt

* copy the application code

* expose the app port

* start the FastAPI app with Uvicorn

Keep it straightforward and production-like enough for a lab, but not complex.

The application should run on port 8000\.

---

## **Local run requirements**

The repo must be easy to run locally.

The README should include instructions for:

### **Run without Docker**

* create a virtual environment

* install requirements

* run the app

* open the browser

### **Run with Docker**

* build the image

* run the container

* open the browser

Make sure these instructions are tested and accurate.

---

## **README requirements**

Write a clean README that explains:

* what the project is

* what routes it has

* what environment variables it supports

* how to run it locally without Docker

* how to run it with Docker

* what interns are expected to modify

The README should also clearly tell Engineers that they are expected to update the displayed values for:

* their name

* cloud platform

* environment if required

* version if required

Do not include cloud deployment steps in this repo README.

Those belong to the lab instructions, not the starter app repo.

---

## **What interns should be able to modify easily**

The project makes it obvious where changes will be made.

That means:

* environment variable names should be easy to spot

* the homepage template should be simple

* no hidden logic

* no unnecessary abstraction

The starter repo should feel approachable.

---

## **Code quality requirements**

The code should be:

* clean

* readable

* small

* well-organized

* beginner-friendly

* lightly commented where useful

Do not make it too clever.

Avoid:

* unnecessary classes

* complex config systems

* advanced dependency injection

* database integration

* authentication

* background workers

* queues

* external APIs

This is only for iac-lab\.

---

## **Important constraints**

Do not add:

* database

* login system

* admin panel

* JavaScript frontend framework

* React

* Vue

* Redis

* Celery

* message queue

* Terraform

* cloud-specific deployment files

This repository is only the starter application code that will later be containerized and deployed.

---

## **Deliverables Codex must create**

Codex should generate:

* the application source code

* HTML template

* minimal CSS styling

* requirements.txt

* Dockerfile

* .dockerignore

* .gitignore

* README.md

Everything should be complete and runnable.

---

## **Success criteria**

The starter repo is successful if:

* the app runs locally without errors

* the homepage loads in a browser

* the homepage displays the required fields

* the values come from environment variables

* /health returns HTTP 200

* Docker build works

* Docker run works

* the README is clear

* the repo is simple enough for quick understanding

## 

Here is the repo link:  
[https://github.com/celestinaodili/project-app.git](https://github.com/celestinaodili/project-app.git)

You should push the code here.
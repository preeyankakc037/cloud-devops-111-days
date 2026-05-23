# Day 40: Containers and Kubernetes (Code for Change Challenge)

## What I Learned Today

Today I learned how modern applications are packaged and managed using containers and Kubernetes. This helps in running applications consistently and scaling them easily.

## 1. Containers (Simple Understanding)

A container is a lightweight package that includes:

* Application code
* Libraries
* Dependencies

It runs the same everywhere (local, cloud, production).

Flow:

Developer Code
↓
Docker Image (build)
↓
Container (run)

## 2. Containers vs Virtual Machines

Virtual Machine:

* Has full OS
* Heavy and slow

Container:

* Shares host OS
* Lightweight and fast

## 3. Docker (What I Understood)

Docker is used to create and run containers.

Basic Flow:

Write Dockerfile
↓
Build Image
↓
Run Container

Key Terms:

* Image: Blueprint
* Container: Running app

## 4. Why Containers Matter

* Same environment everywhere
* Faster deployment
* Easy scaling
* Better resource usage

## 5. Kubernetes (Main Idea)

Kubernetes helps manage multiple containers automatically.

It solves problems like:

* Managing many containers
* Scaling apps
* Handling failures

## 6. Kubernetes Architecture (Basic Flow)

User Request
↓
API Server (Control Plane)
↓
Scheduler decides node
↓
Pod runs on Worker Node

## 7. Key Kubernetes Components

Pod:

* Smallest unit
* Runs container

Deployment:

* Maintains number of pods

Service:

* Exposes application

## 8. Scaling Concept

If traffic increases:

1 Pod → 3 Pods → 10 Pods

Kubernetes handles this automatically (Auto Scaling)

## 9. Self-Healing Concept

If a container crashes:

Pod Fails
↓
Kubernetes detects
↓
New Pod created automatically

## 10. Containers in AWS

I also learned AWS services for containers:

* ECS: Simple container service
* EKS: Kubernetes on AWS
* Fargate: Serverless containers (no server management)

## 11. ECS vs EKS (Simple)

ECS:

* Easy to use
* AWS controlled

EKS:

* Uses Kubernetes
* More flexible

## Final Understanding

Today I understood how:

* Containers package applications
* Docker helps run them
* Kubernetes manages them at scale
* AWS provides managed container services

## Quick Self Questions

1. What is a container?
2. Why is Docker used?
3. What problem does Kubernetes solve?
4. What is a Pod?
5. What is auto-scaling?
6. Difference between ECS and EKS?

# Day 98 – Kubernetes Resource Management (Requests & Limits)

## Overview  
Today I learned how Kubernetes manages resources like CPU and memory for containers. After understanding health checks, I wanted to see how Kubernetes ensures that applications don’t consume too many resources or affect others.

## My Understanding  
I realized that without proper limits, one container can use excessive resources and impact the entire system. Kubernetes solves this by allowing us to define resource requests and limits for each container.

## What I Did  

I explored how to define CPU and memory requests and limits inside a deployment YAML file. I understood how Kubernetes schedules pods based on requested resources and how limits prevent overuse.

I also observed how containers behave when they exceed memory limits and how Kubernetes handles such situations.

## Key Concepts  

Resource Requests  
The minimum amount of CPU and memory a container needs. Kubernetes uses this for scheduling.

Resource Limits  
The maximum amount of CPU and memory a container can use.

Scheduling  
Kubernetes places pods on nodes based on available resources.

OOM (Out Of Memory)  
If a container exceeds memory limits, it may be terminated and restarted.

## Commands / Areas I Practiced  

kubectl describe pod  
kubectl get pods  
kubectl apply -f  

## Realization  

This helped me understand how Kubernetes maintains fairness and stability in a cluster. Proper resource management is very important for production environments.

## Summary  
Today I learned how to manage CPU and memory using requests and limits in Kubernetes. This ensures efficient resource usage and prevents system overload.
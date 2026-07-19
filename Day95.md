# Day 95 – Kubernetes Monitoring Basics (Metrics & Observability)

## Overview  
Today I explored how to monitor applications running in Kubernetes. After learning how to deploy and manage apps, I realized monitoring is essential to understand performance and detect issues early.

## My Understanding  
I understood that running applications is not enough—we also need visibility into how they behave. Kubernetes provides basic metrics, and tools can be added to track CPU, memory, and overall health.

## What I Did  

I explored how to check resource usage of nodes and pods. I learned about the Metrics Server and how it enables commands to view CPU and memory consumption.

I also looked into how monitoring tools like Prometheus and Grafana are commonly used, even though I didn’t fully set them up yet.

## Key Concepts  

Metrics Server  
A Kubernetes component that collects resource usage data.

Resource Monitoring  
Tracking CPU and memory usage of pods and nodes.

Observability  
Understanding system behavior through metrics, logs, and traces.

Basic Health Checks  
Monitoring helps identify failing or overloaded components.

## Commands I Practiced  

kubectl top nodes  
kubectl top pods  
kubectl describe pod  

## Realization  

This made me realize that deploying applications is only part of the job. Monitoring is equally important to ensure everything runs smoothly and to quickly debug issues.

## Summary  
Today I learned the basics of Kubernetes monitoring and explored how to check resource usage. This is an important step toward managing production systems effectively.
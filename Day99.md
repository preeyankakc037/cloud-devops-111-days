# Day 99 – Kubernetes Autoscaling (Horizontal Pod Autoscaler)

## Overview  
Today I explored autoscaling in Kubernetes. After learning how to manage resources, I wanted to understand how Kubernetes can automatically adjust based on application load.

## My Understanding  
I realized that in real-world applications, traffic is not constant. Sometimes load increases, and sometimes it decreases. Instead of manually scaling pods, Kubernetes can do this automatically using the Horizontal Pod Autoscaler (HPA).

## What I Did  

I studied how HPA works and how it uses metrics like CPU utilization to decide when to scale pods up or down. I explored how to configure autoscaling for a deployment and how Kubernetes adjusts the number of replicas dynamically.

Even though I didn’t fully stress-test it, I understood the workflow of how scaling decisions are made.

## Key Concepts  

Horizontal Pod Autoscaler (HPA)  
Automatically adjusts the number of pod replicas based on resource usage.

Scaling Based on Metrics  
Commonly uses CPU utilization, but can also use custom metrics.

Dynamic Scaling  
Pods increase during high load and decrease when load is low.

Efficiency  
Helps optimize resource usage and cost in real environments.

## Commands I Explored  

kubectl autoscale deployment  
kubectl get hpa  
kubectl describe hpa  

## Realization  

This felt like a very powerful feature. Instead of worrying about handling traffic manually, Kubernetes can scale applications automatically, making systems more efficient and reliable.

## Summary  
Today I learned about Kubernetes autoscaling using HPA. I understood how applications can automatically scale based on demand, which is essential for handling real-world traffic.
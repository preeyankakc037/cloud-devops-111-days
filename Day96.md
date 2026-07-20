# Day 96 – Kubernetes Logging and Debugging

## Overview  
Today I focused on logging and debugging in Kubernetes. After learning monitoring basics, I wanted to understand how to actually investigate issues when something goes wrong inside a cluster.

## My Understanding  
I realized that when applications fail, logs are the first place to look. Kubernetes provides simple but powerful commands to access logs and debug containers without needing direct access to the system.

## What I Did  

I explored how to fetch logs from running pods and observed how application output is captured. I also learned how to describe resources to get detailed information about what is happening behind the scenes.

I practiced executing commands inside a running container, which helped me understand how to debug issues in real time.

## Key Concepts  

Logs in Kubernetes  
Applications running inside containers send output to logs, which can be accessed using kubectl.

Debugging Pods  
Using commands to inspect pod status, events, and errors.

kubectl exec  
Allows running commands inside a container for troubleshooting.

Describing Resources  
Provides detailed information about deployments, pods, and services.

## Commands I Practiced  

kubectl logs  
kubectl describe pod  
kubectl exec -it  
kubectl get events  

## Realization  

This was a very practical learning because issues are inevitable in real systems. Knowing how to debug and read logs gives confidence to handle failures effectively.

## Summary  
Today I learned how to view logs and debug applications in Kubernetes. This helped me understand how to identify and fix issues in a running system.
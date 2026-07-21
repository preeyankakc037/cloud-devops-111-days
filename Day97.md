# Day 97 – Kubernetes Health Checks (Liveness & Readiness Probes)

## Overview  
Today I learned about health checks in Kubernetes. After understanding logging and debugging, I wanted to know how Kubernetes automatically detects if an application is healthy or not.

## My Understanding  
I realized that Kubernetes doesn’t just run applications—it continuously checks their health. If something goes wrong, it can restart containers or stop sending traffic to them. This is done using liveness and readiness probes.

## What I Did  

I explored how to define liveness and readiness probes inside a deployment YAML file. I understood different ways to perform health checks like HTTP requests, command execution, and TCP checks.

I also observed how Kubernetes behaves when a container fails a health check and how it tries to recover automatically.

## Key Concepts  

Liveness Probe  
Checks if the application is running. If it fails, Kubernetes restarts the container.

Readiness Probe  
Checks if the application is ready to serve traffic. If it fails, traffic is stopped temporarily.

Self-Healing  
Kubernetes automatically fixes unhealthy containers using probes.

Types of Probes  
HTTP, TCP, and command-based checks for flexibility.

## Commands / Areas I Practiced  

kubectl describe pod  
kubectl get pods  
kubectl apply -f  

## Realization  

This made me understand how Kubernetes ensures reliability. Instead of manually checking applications, Kubernetes continuously monitors and takes action automatically.

## Summary  
Today I learned about liveness and readiness probes and how Kubernetes uses them to maintain application health. This is a key concept for running stable applications in production.
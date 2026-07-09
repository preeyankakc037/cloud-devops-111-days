# Day 85 – Understanding Kubernetes Services in Depth

## Overview

Today I focused on Kubernetes services in more detail. I had already used services to expose applications, but I wanted to properly understand how they actually work and why they are needed.

## My Understanding

I realized that pods in Kubernetes are not stable. Their IP addresses can change when they are recreated. Because of this, directly connecting to pods is not reliable. Services solve this problem by providing a stable way to access applications.

## What I Did

I worked with different types of services and observed how they expose applications. I created services for my deployments and tested how traffic is routed to different pods. I also checked how Kubernetes automatically balances requests between multiple pods.

## Key Concepts

ClusterIP
This is the default service type. It allows communication inside the cluster only.

NodePort
This exposes the application on a specific port of the node, making it accessible from outside.

Load Balancing
Services distribute traffic across multiple pods, which improves performance and reliability.

Service Discovery
Kubernetes allows services to be accessed using names instead of IP addresses.

## Commands I Practiced

kubectl expose deployment
kubectl get services
kubectl describe service

## Realization

Today helped me understand how communication works in Kubernetes. Without services, managing connections between different parts of an application would be difficult. This made me see how important services are in real deployments.

## Summary

Today I explored Kubernetes services in depth and understood how they provide stable access to applications. I practiced exposing deployments and learned how traffic is managed across pods.

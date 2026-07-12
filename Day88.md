# Day 88 – Understanding Kubernetes Ingress

## Overview

Today I learned about Ingress in Kubernetes, which helped me understand how applications are exposed in a more advanced and production-ready way. Until now, I was using NodePort, but that approach has limitations.

## My Understanding

I realized that NodePort is not ideal for real-world applications because it exposes services on different ports. Ingress provides a cleaner way to manage external access using a single entry point, usually with domain-based routing.

## What I Did

I studied how Ingress works and how it routes traffic to different services based on rules. I also explored the concept of an Ingress Controller, which is required to make Ingress work.

Even though I didn’t fully implement it yet, I understood how it connects everything together in a real deployment.

## Key Concepts

Ingress
A resource that manages external access to services, usually via HTTP or HTTPS.

Ingress Controller
A component that actually processes Ingress rules and routes traffic.

Routing Rules
Ingress allows routing based on paths or domain names.

Centralized Access
Instead of exposing multiple services separately, Ingress provides a single entry point.

## Commands I Explored

kubectl get ingress
kubectl describe ingress

## Realization

This felt like a more production-level concept. I now understand how large applications manage external traffic in a clean and scalable way instead of relying on basic exposure methods.

## Summary

Today I learned about Kubernetes Ingress and how it provides a better way to expose applications. It gave me insight into how real-world systems handle routing and external access.

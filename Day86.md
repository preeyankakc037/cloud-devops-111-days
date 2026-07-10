# Day 86 – Understanding Kubernetes Namespaces

## Overview

Today I learned about namespaces in Kubernetes. Until now, I was working in the default setup without thinking much about organization, but today I understood how Kubernetes manages multiple environments using namespaces.

## My Understanding

I realized that namespaces help in organizing resources inside a cluster. When multiple applications or teams are working on the same cluster, things can get messy. Namespaces help separate everything logically.

## What I Did

I checked the existing namespaces in my cluster and noticed the default ones. Then I created my own namespace and deployed an application inside it. I also tried listing resources within that namespace to see how isolation works.

## Key Concepts

Namespace
A way to divide cluster resources into separate environments.

Default Namespace
If no namespace is specified, resources are created here.

Resource Isolation
Resources inside one namespace do not interfere with others.

Multi Environment Setup
Namespaces can be used for dev, testing, and production environments.

## Commands I Practiced

kubectl get namespaces
kubectl create namespace
kubectl get pods -n
kubectl apply -f with namespace

## Realization

This made me understand how large teams manage Kubernetes clusters. Instead of creating multiple clusters, they organize everything using namespaces. It keeps things clean and manageable.

## Summary

Today I learned how namespaces work in Kubernetes and how they help organize resources. I practiced creating and using namespaces, which is important for managing real-world applications.

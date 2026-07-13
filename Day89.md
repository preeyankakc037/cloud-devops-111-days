# Day 89 – Understanding Kubernetes Persistent Volumes

## Overview

Today I went deeper into how Kubernetes handles storage. Earlier I learned about Docker volumes, and today I connected that knowledge with Kubernetes by understanding persistent storage.

## My Understanding

I realized that just like containers in Docker, pods in Kubernetes are also temporary. If a pod is deleted, any data inside it is lost. To solve this, Kubernetes provides Persistent Volumes, which allow data to exist independently of pods.

## What I Did

I explored how Persistent Volumes and Persistent Volume Claims work together. I understood the relationship between storage resources and applications. I also looked at how a pod can request storage and use it without worrying about where it is coming from.

## Key Concepts

Persistent Volume
A storage resource in the cluster that exists independently of pods.

Persistent Volume Claim
A request for storage made by a pod. It defines how much storage is needed.

Decoupled Storage
Storage is managed separately from compute, making applications more flexible.

Reusability
Data remains safe even if pods are deleted and recreated.

## Commands I Explored

kubectl get pv
kubectl get pvc
kubectl describe pv
kubectl describe pvc

## Realization

This was an important concept because real applications like databases cannot lose data. Understanding persistent storage made me see how Kubernetes can handle stateful applications.

## Summary

Today I learned about Persistent Volumes and Persistent Volume Claims in Kubernetes. I understood how storage works independently from pods, which is essential for running real-world applications.

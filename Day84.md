# Day 84 – Managing Kubernetes Deployments and Scaling

## Overview

Today I focused on working more deeply with deployments in Kubernetes. Earlier, I created deployments, but today I explored how to manage and scale them properly.

## My Understanding

I realized that deployments are not just for running applications, they are used to maintain stability and handle changes. Kubernetes makes sure that the desired number of pods are always running, even if something fails.

## What I Did

I worked with an existing deployment and tried scaling it up and down. I increased the number of replicas and saw new pods being created automatically. Then I reduced the replicas and observed how Kubernetes removed extra pods safely.

I also updated the deployment image and saw how Kubernetes handled rolling updates without stopping the application.

## Key Concepts

Scaling
Changing the number of replicas based on requirement. This helps handle load and improve availability.

Rolling Updates
Updating applications without downtime. Kubernetes replaces old pods with new ones gradually.

Self Healing
If a pod fails, Kubernetes automatically creates a new one to maintain the desired state.

Desired State
Kubernetes always tries to match the current state with what is defined in the configuration.

## Commands I Practiced

kubectl scale deployment
kubectl set image
kubectl rollout status
kubectl rollout history

## Realization

This was a very practical learning. I saw how Kubernetes handles real-world scenarios like scaling and updates automatically. It gave me a clearer understanding of how applications stay available even during changes.

## Summary

Today I learned how to manage and scale deployments in Kubernetes. I practiced scaling, updating applications, and observed how Kubernetes maintains stability, which is a key part of DevOps in production.

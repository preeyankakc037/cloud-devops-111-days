# Day 82 – Finally Running Kubernetes Locally

## Overview

Today was a satisfying day because after struggling with setup issues for the past few days, I was finally able to get Docker and Kubernetes running on my system. It took some time, but things started working, and I could move forward again.

## My Understanding

Fixing the WSL and Docker issues helped me understand how everything is connected under the hood. Once the setup was stable, Kubernetes commands started working smoothly, which made all the earlier effort worth it.

## What I Did

I verified that Docker was running properly and that Kubernetes was enabled. After that, I checked the cluster status and confirmed that my node was ready. Then I deployed a simple application to test everything.

I created a deployment using an Nginx image and checked if the pods were running. After that, I exposed the application and accessed it in the browser, which confirmed that everything was working fine.

## Key Concepts

Cluster Verification
I used commands to check whether the Kubernetes cluster was up and running.

Deployments
I created a deployment to manage my application instead of directly creating pods.

Pods
I monitored the pods to see if they were running correctly.

Service Exposure
I exposed my application so that it could be accessed from my local system.

## Commands I Practiced

kubectl get nodes
kubectl create deployment
kubectl get pods
kubectl expose deployment

## Realization

This felt like a breakthrough moment. After a few slow days due to setup issues, I was finally able to run Kubernetes practically. It gave me confidence that I can now move ahead with more advanced topics.

## Summary

Today I successfully fixed my environment and ran Kubernetes locally. I deployed my first application and verified that everything was working, which marked a strong comeback in my DevOps journey.

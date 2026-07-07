# Day 83 – Understanding Kubernetes YAML Files

## Overview

Today I moved from running Kubernetes commands to writing YAML files. Until now, I was creating deployments and services using CLI commands, but today I learned the proper and more practical way to define everything.

## My Understanding

I realized that in real-world DevOps, people don’t rely on commands for everything. Instead, they define configurations in YAML files so that setups can be reused, version controlled, and shared easily.

## What I Did

I created my first YAML file for a deployment. I defined things like the image, number of replicas, and container details. Then I applied it using kubectl and saw my application running.

I also explored how to define a service in YAML to expose the application. Writing everything in a file felt more structured compared to running commands.

## Key Concepts

YAML Configuration
A declarative way to define Kubernetes resources instead of using commands.

apiVersion and kind
These define what type of resource I am creating and which version of Kubernetes API is being used.

Metadata
Used to give names and labels to resources.

Spec
This is the most important section where the actual configuration is defined.

Declarative Approach
Instead of telling Kubernetes what to do step by step, I define the desired state and Kubernetes manages it.

## Commands I Practiced

kubectl apply -f
kubectl get all
kubectl delete -f

## Realization

This felt like a shift toward real DevOps practices. YAML files make everything cleaner and more manageable. I can now save my configurations and reuse them anytime instead of rewriting commands.

## Summary

Today I learned how to use YAML files in Kubernetes to create deployments and services. This made my workflow more structured and closer to how things are done in real projects.

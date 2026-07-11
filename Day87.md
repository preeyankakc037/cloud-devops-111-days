# Day 87 – Working with Kubernetes ConfigMaps and Secrets

## Overview

Today I explored how Kubernetes handles configuration data. Until now, I was putting everything directly inside my deployment files, but today I learned a better and more secure way to manage configurations.

## My Understanding

I realized that separating configuration from application code is very important. Instead of hardcoding values like environment variables, Kubernetes provides ConfigMaps and Secrets to manage them properly.

## What I Did

I created a ConfigMap and used it inside a deployment to pass environment variables to my application. After that, I explored Secrets and understood how sensitive data like passwords and API keys should be handled.

I also updated my deployment to use these configurations and saw how flexible it becomes when changes are needed.

## Key Concepts

ConfigMap
Used to store non-sensitive configuration data like environment variables and application settings.

Secrets
Used to store sensitive data securely such as passwords, tokens, and keys.

Decoupling Configuration
Separating config from application makes it easier to manage and update without changing the application itself.

Environment Variables
ConfigMaps and Secrets can be injected into containers as environment variables.

## Commands I Practiced

kubectl create configmap
kubectl create secret
kubectl get configmap
kubectl get secret

## Realization

This was an important step because now I understand how real applications handle configuration. It also made me realize how important security is when working with production systems.

## Summary

Today I learned how to use ConfigMaps and Secrets in Kubernetes to manage application configuration and sensitive data. This made my deployments more flexible, secure, and closer to real-world practices.

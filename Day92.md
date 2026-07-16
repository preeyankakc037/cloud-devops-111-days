# Day 92 – Introduction to Helm (Kubernetes Package Manager)

## Overview

Today I learned about Helm, which is known as the package manager for Kubernetes. After working with multiple YAML files, I realized things can become complex quickly, and Helm helps simplify that process.

## My Understanding

I understood that managing many Kubernetes YAML files manually is not efficient, especially for large applications. Helm solves this by packaging all configurations into reusable templates called charts.

## What I Did

I explored the basics of Helm and how it works. I learned about Helm charts and how they define Kubernetes resources in a structured way. I also looked into how values can be customized without changing the main templates.

Even though I didn’t go very deep into implementation, I got a clear idea of how Helm simplifies deployments.

## Key Concepts

Helm
A tool that helps manage Kubernetes applications using packages.

Charts
Pre-configured templates that define Kubernetes resources.

Values.yaml
A file used to customize configurations without editing templates directly.

Reusability
Helm allows the same setup to be reused across different environments.

## Commands I Explored

helm create
helm install
helm list
helm uninstall

## Realization

This felt like an important step toward real DevOps practices. Writing raw YAML files is good for learning, but Helm makes things much more efficient and scalable.

## Summary

Today I learned the basics of Helm and how it simplifies Kubernetes deployments. It gave me an understanding of how real-world applications are managed more efficiently.

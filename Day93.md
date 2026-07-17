# Day 93 – Working with Helm Charts Practically

## Overview

Today I moved from just understanding Helm concepts to actually working with Helm charts. After learning what Helm is yesterday, I wanted to see how it works in practice.

## My Understanding

I realized that Helm is not just about simplifying YAML files, it also helps in managing applications like versions, upgrades, and rollbacks. This makes deployments much more flexible compared to using raw Kubernetes manifests.

## What I Did

I created a basic Helm chart using the default template and explored its structure. I looked into different files like values.yaml and templates folder to understand how everything is connected.

I then installed a chart into my Kubernetes cluster and verified that all resources like deployments and services were created automatically. After that, I tried modifying values and re-deploying to see how changes are applied.

## Key Concepts

Helm Chart Structure
Understanding folders like templates, values.yaml, and Chart.yaml.

Template Rendering
Helm dynamically generates Kubernetes YAML files using templates.

Values Customization
Changing configurations easily through values.yaml without touching core templates.

Release Management
Helm tracks installations as releases, making it easy to manage them.

## Commands I Practiced

helm install
helm upgrade
helm list
helm uninstall

## Realization

This was a very practical learning day. I saw how Helm can save a lot of time and effort, especially when dealing with complex applications. It made Kubernetes feel more manageable.

## Summary

Today I worked hands-on with Helm charts and understood how to create, install, and manage them. This helped me move closer to real-world Kubernetes deployment practices.

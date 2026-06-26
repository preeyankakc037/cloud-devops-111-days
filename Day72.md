# Day 72 – Understanding Docker Images and Containers Clearly

## Overview

Today I focused on clearing one of the most confusing parts of Docker for me — the difference between images and containers. Earlier, I was using commands but not fully understanding what was happening behind the scenes.

## My Understanding

I realized that a Docker image is like a blueprint or template, and a container is the running instance of that image. This simple distinction made everything click.

## What I Learned

I explored how images are built and how containers are created from them. I also understood that multiple containers can be created from the same image, which makes Docker very flexible.

## Key Concepts

**Docker Image**
An image is a read-only file that contains everything needed to run an application, including code, libraries, and dependencies.

**Docker Container**
A container is a running instance of an image. It is isolated and behaves like a small system.

**Image vs Container**
Image is static, container is dynamic. Image does not change, but containers can be started, stopped, and modified.

**Docker Hub**
I understood that images are stored in Docker Hub and can be pulled anytime.

## What I Practiced

* Pulled an image from Docker Hub
* Ran multiple containers from the same image
* Observed how each container runs independently

## Realization

This was an important day because now Docker makes more sense. Before this, I was just running commands. Now I understand what is actually happening.

## Summary

Today I clearly understood the difference between Docker images and containers and practiced using them. This helped me build a strong foundation for upcoming Docker concepts.

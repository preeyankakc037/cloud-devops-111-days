# Day 74 – Understanding Docker Volumes and Data Persistence

## Overview

Today I learned something very important that made Docker feel more practical and real. Until now, I was running containers, but I did not think much about what happens to the data inside them. Today I explored how Docker handles data and why persistence matters.

## My Understanding

I realized that containers are temporary by nature. If a container is removed, all the data inside it is lost. This made me understand that running applications like databases inside containers would be risky without a proper solution. That is where Docker volumes come in.

## What I Did

I first created a container and added some data inside it. After removing the container, I noticed that everything was gone. Then I created a Docker volume and attached it to a new container. This time, even after removing the container, the data was still there. That was the moment things really made sense.

## Key Concepts

Docker Volumes
Volumes are used to store data outside the container so that it is not lost when the container stops or gets deleted.

Bind Mounts
I also came across bind mounts, which connect a local folder from my system to the container. This gives more control but is less managed compared to volumes.

Data Persistence
This is the idea that data should survive even after containers are removed. It is very important for real applications.

Sharing Data
Volumes can also be used to share data between multiple containers, which is useful in many scenarios.

## Commands I Practiced

docker volume create
docker run with volume mapping
docker volume ls

## Realization

This was a very important learning because now I understand how real applications run on Docker without losing data. It is not just about running containers, but also about managing what is inside them.

## Summary

Today I learned how Docker volumes work and why data persistence is important. I practiced creating volumes and attaching them to containers, which helped me understand how to safely store data in Docker.

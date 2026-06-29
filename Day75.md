# Day 75 – Working with Docker Networking

## Overview

Today I explored how containers communicate with each other. Until now, I was running containers individually, but I had not really thought about how they connect in a real application setup. Today’s learning helped me understand how multiple containers can work together.

## My Understanding

I realized that Docker provides its own networking system that allows containers to talk to each other. This is important because in real projects, applications are not just one container. There can be a backend, database, and frontend all running separately but still connected.

## What I Did

I started by checking the default network Docker creates. Then I created my own custom network and ran multiple containers inside it. I tested communication between them and saw how easily containers can connect using names instead of IP addresses.

## Key Concepts

Docker Network
A system that allows containers to communicate with each other in an isolated environment.

Bridge Network
The default network type where containers can communicate if they are on the same network.

Custom Network
Creating my own network gave me better control and made communication simpler between containers.

Container Communication
I understood that containers can talk to each other using container names, which makes things easier than dealing with IP addresses.

## Commands I Practiced

docker network ls
docker network create
docker run with network option
docker network inspect

## Realization

This learning made Docker feel much closer to real-world applications. I now understand how multiple services can run independently but still stay connected. It also gave me a clearer picture of how microservices work in practice.

## Summary

Today I learned how Docker networking works and how containers communicate with each other. I practiced creating networks and connecting multiple containers, which is an important step toward building real applications.

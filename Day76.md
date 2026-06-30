# Day 76 – Introduction to Docker Compose

## Overview

Today I learned about Docker Compose, and it honestly felt like a big upgrade from running containers manually. Until now, I was starting containers one by one using commands, but today I saw how to manage multiple containers in a much cleaner way.

## My Understanding

I realized that Docker Compose is used to define and run multi-container applications using a single file. Instead of writing long commands again and again, I can describe everything in a simple YAML file and run the entire setup in one go.

## What I Did

I created a basic docker-compose.yml file where I defined multiple services. I tried setting up a simple application with a web service and a database. Then I used a single command to bring everything up, and it worked smoothly.

## Key Concepts

Docker Compose
A tool used to manage multiple containers together using a configuration file.

docker-compose.yml
This file contains all the service definitions, networks, and volumes required for the application.

Services
Each container in Compose is defined as a service. For example, a backend, frontend, or database.

Single Command Execution
Instead of running multiple docker run commands, I can start everything using docker compose up.

## Commands I Practiced

docker compose up
docker compose down
docker compose ps

## Realization

This made things feel much more organized. Running multiple containers manually was getting confusing, but Compose simplifies everything. It feels like the right way to manage applications in development.

## Summary

Today I learned how to use Docker Compose to manage multi-container applications. I created my first compose file and ran multiple services together, which made the workflow much easier and cleaner.

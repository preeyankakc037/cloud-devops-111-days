# Day 64 – Understanding Monitoring & Observability

## Overview

Today I focused on monitoring and observability. Instead of just deploying applications, I started thinking about how to track what is actually happening after deployment.

## My Understanding

I realized that deploying an application is not the end. Once the app is live, we need visibility into performance, errors, and user behavior. This is where monitoring becomes critical.

## What I Learned

When I run an application, I need answers to questions like:

* Is my application healthy?
* Are users facing errors?
* Is performance degrading?

Monitoring helps answer these questions in real time.

## Key Concepts

**Monitoring**
I understood monitoring as collecting metrics like CPU usage, memory, request count, and latency. It gives a high-level view of system health.

**Logging**
Logs help me debug issues. Whenever something fails, logs provide detailed information about what went wrong.

**Observability**
This goes beyond monitoring. It helps me understand *why* something is happening inside the system using:

* Metrics
* Logs
* Traces

## Realization

Earlier, I thought deployment was the final step. But now I see that:

* Deployment is just the beginning
* Monitoring ensures reliability
* Observability helps in deep debugging

## Summary

Today shifted my mindset from just building and deploying to actually *understanding and maintaining* systems in production. Monitoring and observability are essential for building reliable applications.

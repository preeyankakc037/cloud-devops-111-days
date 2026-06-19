# Day 65 – Alerting & Incident Response

## Overview

After learning about monitoring, today I moved to the next step — alerting and incident response. Monitoring tells me what is happening, but alerting ensures I take action at the right time.

## My Understanding

I realized that just collecting metrics is not enough. If something breaks and I don’t notice it, monitoring has no value. Alerting helps me react immediately when something goes wrong.

## What I Learned

When running applications, I need to define conditions like:

* High CPU usage
* Increased error rates
* Slow response time

If these thresholds are crossed, alerts should notify me.

## Key Concepts

**Alerting**
I understood that alerts are triggered based on predefined rules. These alerts can notify through:

* Email
* Slack
* SMS

**Thresholds**
Setting proper limits is important. Too sensitive → too many alerts. Too loose → missed issues.

**Incident Response**
Once an alert is triggered:

* Identify the issue
* Debug using logs and metrics
* Fix and restore the service

## Realization

Earlier, I thought fixing bugs manually was enough. Now I see:

* Systems should notify me automatically
* Quick response reduces downtime
* Proper alerting prevents major failures

## Summary

Today I learned that alerting bridges the gap between monitoring and action. It ensures that issues are not just observed but handled quickly, making systems more reliable.

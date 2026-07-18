# Day 94 – Helm Advanced Concepts and Release Management

## Overview  
Today I went deeper into Helm and explored more advanced concepts. After learning how to create and use Helm charts, I focused on how Helm manages application versions and handles updates in a controlled way.

## My Understanding  
I realized that Helm is not just for installing applications, it is also a powerful tool for managing their lifecycle. It keeps track of changes, allows upgrades, and even lets us roll back to previous versions if something goes wrong.

## What I Did  

I worked with Helm releases and explored how upgrades work. I modified values in my chart and used Helm to upgrade the application. I also checked the release history and tried rolling back to a previous version.

This gave me a clear idea of how safe deployments are handled in real environments.

## Key Concepts  

Helm Releases  
Every installation of a chart is tracked as a release, which helps in managing versions.

Upgrades  
Helm allows updating applications without redeploying everything from scratch.

Rollback  
If something breaks after an update, Helm can revert to a previous working version.

Version Control  
Helm maintains a history of changes, making deployments more reliable.

## Commands I Practiced  

helm upgrade  
helm rollback  
helm history  
helm status  

## Realization  

This was an important learning because it showed how real-world systems handle updates safely. Instead of worrying about breaking changes, tools like Helm provide control and confidence.

## Summary  
Today I explored advanced Helm features like upgrades, rollbacks, and release management. This helped me understand how applications are maintained and updated reliably in Kubernetes.
# Overview

Here we'll explore some of the common tasks that developers perform with OpenShift. You'll become familiar with how to use environment variables, secrets, build configurations, and more-- basic things a developer might care about for their apps.

### Steps (CLI)

1. $ `oc status`
1. $ `oc describe deploymentconfig/dc-metro-map`
1. $ `oc describe rc -l app=dc-metro-map`
1. $ `oc describe is -l app=dc-metro-map`
1. $ `oc describe pod`
1. $ `oc describe bc/dc-metro-map`
1. $ `oc describe build/dc-metro-map-1`
1. $ `oc get pods`
1. $ `oc logs dc-metro-map-1-build`
1. $ `oc set env deploymentconfig/dc-metro-map -e BEERME=true`
1. $ `oc get pods -w`
1. $ `oc get pods`
1. $ `oc exec -it <RUNNING_POD> -- /bin/bash`
1. $ `env | grep BEER`
1. $ `exit` # !Make sure your are in the pod when you run this!

### Steps (Console)

https://redhatgov.io/workshops/openshift_4_101/lab4-devmanage/

# Summary

In this module you've seen how to trace running software back to its roots, how to see details on the pods running your software, how to update deployment configurations, how to inspect logs files, how to set environment variables consistently across your environment, and how to interactively attach to running containers. All these things should come in handy for any developer working on an OpenShift platform.

# [Module 03 <<](../Module%2003%20-%20Deploying%20via%20S2I) | [>> NEXT: Module 05 - Rollbacks](../Module%2005%20-%20Rollbacks)

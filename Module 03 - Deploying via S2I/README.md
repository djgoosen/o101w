# Module 03 - Deploying via S2I

## Module Overview

A big differentiator for OpenShift over upstream Kubernetes is its Source to Image (S2I) capability. S2I is a framework that makes it easy to turn your source code into runnable images. And a key advantage of using S2I is how easy it makes using images for developers.

So let's build a Node.js web app, using S2I.

### Steps (CLI)

1. $ `oc new-app --name=dc-metro-map https://github.com/RedHatGov/openshift-workshops.git --context-dir=dc-metro-map --as-deployment-config=true`
1. $ `oc expose service dc-metro-map`
1. $ `oc get builds`
1. $ `oc logs builds/dc-metro-map-1`
1. $ `oc project`
1. $ `oc status`
1. $ `oc get routes`
1. BROWSE: http://dc-metro-map-demo-31.apps-crc.testing/

### Steps (Web Console)

https://redhatgov.io/workshops/openshift_4_101/lab3-s2i/

# Summary

In this lab we deployed a sample application using S2I. This process built our code and put it into an image. It then deployed the image into our OpenShift platform in a pod, and exposed a route to allow outside web traffic to access our new app. 

# [Module 02 <<](../Module%2002%20-%20Your%20First%20Pod) | [>> NEXT: Module 04 - Developing and Managing Your App](../Module%2004%20-%20Developing%20and%20Managing%20Your%20App)

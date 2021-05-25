# Overview

Here we will discuss how OpenShift supports three key development and deployment best practices: labels, CI/CD pipelines, and blue/green deployments.

### Steps

#### Labels

You can use labels to organize, group, or select API objects.

For example, pods are "tagged" with labels, and then services use label selectors to identify the pods they proxy to. This makes it possible for services to reference groups of pods, even treating pods with potentially different docker containers as related entities.

1. $ `oc get pods`
1. $ `oc describe pod/<PODNAME> | grep Labels: --context=4`
1. $ `oc label pod/<PODNAME> testdate=5.25.2021 testedby=$USER`
1. $ `oc describe pod/<PODNAME> | grep Labels: --context=4`
1. $ `oc delete all -l app=dc-metro-map`
1. $ `oc delete secrets dc-metro-map-generic-webhook-secret dc-metro-map-github-webhook-secret 2>/dev/null`


Now you know that all the objects in OpenShift can be labeled. This is important because those labels can be used as part of your CI/CD process. 

See also: https://redhatgov.io/workshops/openshift_4_101/lab7-labels/

#### CI/CD Pipelines

In modern software projects many teams utilize the concept of Continuous Integration (CI) and Continuous Delivery (CD). By setting up a tool chain that continuously builds, tests, and stages software releases, a team can ensure that their product can be reliably released at any time. OpenShift can be an enabler in the creation and management of this toolchain.

1. $ `brew install tektoncd-cli`
1. https://github.com/openshift/pipelines-tutorial/blob/master/install-operator.md
1. https://github.com/openshift/pipelines-tutorial/

See also: https://redhatgov.io/workshops/openshift_4_101/lab8-cicd/

#### Blue/Green Deployments

When implementing CI/CD, one very useful technique is called blue/green deployments. It addresses the desire to minimize downtime during the release of a new version of an application to production. Essentially, it involves running two production versions of your app side-by-side and then switching the routing from the last stable version to the new version once it is verified. Using OpenShift, this can be seamless because using containers we can easily and rapidly deploy a duplicate infrastructure to support alternate versions and modify routes to a service.

https://redhatgov.io/workshops/openshift_4_101/lab9-bluegreen/

1. $ `oc new-project bluegreen-0`
1. $ `oc new-app --name=green https://github.com/<YOUR_GITHUB_ID>/openshift-workshops --context-dir=dc-metro-map --as-deployment-config=true`
1. $ `oc expose service green`
1. Wait for the application to become available, then navigate to your application and validate it deployed correctly.
1. Release a new app version
1. $ `oc new-app --name=blue https://github.com/<YOUR_GITHUB_ID>/openshift-workshops --context-dir=dc-metro-map --as-deployment-config=true`
1. Wait for the "blue" application to become avialable before proceeding.
1. $ `oc edit route green`
1. This will bring up the Route configuration yaml. Edit the element "spec:". On the "to:" "name:" line, change its value from "green" to "blue".

See also: https://redhatgov.io/workshops/openshift_4_101/lab9-bluegreen/

# [Module 06 <<](../Module%2006%20-%20Replication%20and%20Recovery) | [>> Onward! Download a free 60-day OpenShift Container Platform eval today. ](https://www.openshift.com/try?sc_cid=7013a000002Dfg9AAC)

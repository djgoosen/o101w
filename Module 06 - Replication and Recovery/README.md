# Overview 

Things will go wrong with your software, or your hardware, or from something out of your control. But we can plan for that failure, and planning for it let's us minimize the impact. OpenShift supports this via what we call replication and recovery.

### Replication

Let's walk through a simple example of how the replication controller can keep your deployment at a desired state. Assuming you still have the dc-metro-map project running we can manually scale up our replicas to handle increased user load.

### Steps (CLI)

1. $ `oc scale --replicas=4 dc/dc-metro-map`
1. $ `oc get pods`

So you've told OpenShift that you'd like to maintain 4 running, load-balanced, instances of our web app.

### Recovery

OK, now that we have a slightly more interesting replication state, we can test a service outages scenario. In this scenario, the dc-metro-map replication controller will ensure that other pods are created to replace those that become unhealthy. Let's forcibly inflict an issue and see how OpenShift responds.

1. $ `oc delete pod/<PODNAME>`
1. $ `oc get pods -w`

If you're fast enough you'll see the pod you deleted go "Terminating" and you'll also see a new pod immediately get created and transition from "Pending" to "Running". If you weren't fast enough you can see that your old pod is gone and a new pod is in the list with an age of only a few seconds.

### Application Health

In addition to the health of your application's pods, OpenShift will watch the containers inside those pods. Let's forcibly inflict some issues and see how OpenShift responds.

1. $ `oc describe dc/dc-metro-map`
1. $ `oc get pods`
1. $ `oc exec <PODNAME> -it /bin/bash`
1. $ `pkill -9 node` # !Make sure you are in the pod when you run this!
1. (RUN THE PREVIOUS TWO COMMANDS AGAIN)
1. `oc get pods -w ` # Watch for the pod restart

### Clean up

Let's scale back down to 1 replica. If you are using the web console just click the down arrow from the Deployments Configs Overview page. If you are using the command line use the `oc scale` command.

1. Cleanup - reduce pods via Web or `oc scale --replicas=1 dc/dc-metro-map`

### Steps (Web Console)

https://redhatgov.io/workshops/openshift_4_101/lab6-replicationrecovery/

# Summary

In this module we learned about replication controllers and how they can be used to scale your applications and services. We also tried to break a few things and saw how OpenShift automatically healed the service and keep it running.

# [Module 05 <<](../Module%2005%20-%20Webhooks%20and%20Rollbacks) | [>> NEXT: Module 07 - OpenShift Development Best Practices](../Module%2007%20-%20OpenShift%20Development%20Best%20Practices)

# Module 01: What is OpenShift Used For?

## Some Vocabulary

* **Kubernetes**: an open-source _container_ _orchestration_ system.
* **Container**: your software plus everything else it depends on to run.
* **Orchestration**: the automated configuration, coordination, and management of computer systems and software.
* **OpenShift**: the word's best distribution of _Kubernetes_, made by Red Hat.
* **Image**: a read-only file that is used to create _containers_.
* **Image Stream**: one or more container _images_ identified by labels.
* **Label**: text that is added to container _images_ to give special meaning to users.
* **Pod**: one or more _containers_ that run together. This is the smallest thing that _Kubernetes_ actually _orchestrates_.
* **Service**: provides a common DNS name to access a _pod_ (or set of pods).
* **Project**: a group of _services_ that are related to each other in some way.
* **Application**: any computer software made to help a user to do specific things.
* **Deployment**: any change to your _application_, that is started by a container _image_ change or a configuration change.
* **Build**: the process of turning your source code into an _image_ that _containers_ can be created from.
* **BuildConfig**: configuration data that determines how to manage your _build_.
* **Route**: a labeled and DNS mapped network path to a service from outside OpenShift.
* **Operator**: a way of packaging, deploying and managing a _Kubernetes_ _application_.
* **Cluster**: made up of _control_ and _worker nodes_.
* **Control node**: schedules things that are meant to happen, watches for problems, and _orchestrates_ everything. In the real world, there are usually at least three of these.
* **Worker node**: where the _pods_ run. In the real world, there are usually two or more of these.

## Module Overview

OpenShift POC PDF

# Additional resources:

Related video:

[Level Up: "Installing CodeReady Containers"](https://youtu.be/72Bfw1WxojQ)

Kubernetes glossary: 

https://kubernetes.io/docs/reference/glossary


# [Intro <<](https://github.com/1eve1Up/openshift-workshops/tree/main/101) | [>> NEXT: Module 02 - Your First Pod](../Module%2002%20-%20Your%20First%20Pod)

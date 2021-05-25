# OpenShift 101 Workshop

## Background

This workshop is based in part on: https://redhatgov.io/workshops/openshift_4_101/

## Introduction

The OpenShift 101 workshop uses [CodeReady Containers (CRC)](https://developers.redhat.com/products/codeready-containers/overview), which is "OpenShift 4 on your laptop".

[CRC installation](https://access.redhat.com/documentation/en-us/red_hat_codeready_containers/1.19/html/getting_started_guide/installation_gsg) is currently supported on Windows, macOS and Linux. (Download requires a redhat.com account, which is free to create.)

*During the workshop*, the Level Up team can assist you if you have run into any challenges with the CRC install. However, in order to maximize the time everyone will be spending together on the OpenShift 101 learning modules themselves, we highly recommend that you install CRC prior to the start of the workshop. Your download timing may vary, but CRC install itself should only take a few minutes.

### Your Pre-Steps:

1. (If you don't already have one) create a redhat.com *Personal* account: https://www.redhat.com/wapps/ugc/register.html?_flowId=register-flow&_flowExecutionKey=e1s1

2. Download and install CRC: https://developers.redhat.com/products/codeready-containers/overview

Here's a recent video walkthrough of CRC install on macOS: https://www.youtube.com/watch?v=72Bfw1WxojQ

## To Start This Workshop From Your Laptop (Linux/macOS):

1. Download CodeReady Containers either by clicking the Download button; or: $ `wget https://mirror.openshift.com/pub/openshift-v4/clients/crc/latest/crc-macos-amd64.pkg --user=<YOUR_RH_USERNAME> --ask-pass`
2. Download the Pull Secret (you will be asked to paste this the first time you run crc start).
3. Double-click `crc-macos-amd64.pkg` to launch the the install wizard.
4. Open your Terminal
5. $ `crc setup`
6. $ `crc start`

# [>> NEXT: Module 01 - Module 01 - Overview](Module%2001%20-%20Overview)

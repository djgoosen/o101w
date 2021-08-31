# Overview

Once you have an app deployed in OpenShift you can take advantage of some continuous capabilities that help to enable DevOps and automate your management process. We will cover some of those in this lab: Build triggers, webhooks, and rollbacks.

This module requires a GitHub account. It's free to sign up.

### Steps (Web Consoles)

#### GitHub Steps

1. Fork https://github.com/djgoosen/node-js-example ("Fork a repo": [docs.github.com](https://docs.github.com/en/github/getting-started-with-github/quickstart/fork-a-repo))
2. Copy your forked repo's URL to your clipboard

#### CRC Steps

##### Add the Repo to CRC

1. Click: +Add
1. Click: From Git
1. Git Repo URL: Paste your forked repo's URL here
1. Click: Create
1. Click: Logs
1. Wait until you see "Push successful"
1. Click: Topology
1. Click: the "Open URL" button 

##### Make a Code Change to the GitHub Repo and Rebuild

1. In GitHub... change the text in index.html
1. In CRC... Topology > node-js-example > Resources
1. Start Build
1. Click: Logs
3. Wait until you see "Push successful"
4. Click: Topology
5. Click: the "Open URL" button 
6. Verify the page shows your change 

##### Rollback the Code Change

1. Rollback the change

### Reference Steps

https://redhatgov.io/workshops/openshift_4_101/lab5-rollbacks/

# [Module 04 <<](../Module%2004%20-%20Developing%20and%20Managing%20Your%20App) | [>> NEXT: Module 06 - Replication and Recovery](../Module%2006%20-%20Replication%20and%20Recovery)

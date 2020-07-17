# Hyper Protect Virtual Servers Monitoring Setup

This repo documents one monitoring implementation for the Hyper Protect Virtual Servers V1.2.1 on premises offering. For official product documentation please refer to [the product knowledge center](https://www.ibm.com/support/knowledgecenter/SSHPMH_1.2.x/topics/hpvs121.html).

The product ships with collectd and monitoring images. The expectation is that the user can consume this monitoring data into their own monitoring infastructure. This repo documents the process to build and deploy your own Prometheus and Grafana Virtual Servers through the Secure Build process. If you already have an enterprise Grafana service, you can certainly only choose to deploy the Prometheus piece inside your hosting appliance.


![architecturediagram](images/hpvsmonitoring.png)

The general steps are:
1. Create your own private Github repo for your Prometheus build with the necessary keys and information
2. Go through the Secure Build process to build your Prometheus image
3. Register your Prometheus image with your hosting appliance
4. Deploy and test your Prometheus Virtual Server
5. Go through the Secure Build process to build your Grafana image
6. Register your Grafana image with your hosting appliance
7. Deploy and test your Grafana Virtual Server
8. Import the Hyper Protect Virtual Server Grafana Dashboard and customize static properties to reflect your hosting appliance allocations

This document assumes that you have already completed the following steps:
1. Installed Hyper Protect Virtual Servers 1.2.1
2. Setup the collectd and monitoring containers in your hosting appliance. Refer to the [knowledge center](https://www.ibm.com/support/knowledgecenter/SSHPMH_1.2.x/topics/create_mc.html) for detailed instructions on how to do this.



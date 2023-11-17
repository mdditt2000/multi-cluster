# Multi-Cluster Kubernetes using A/B Deployment

This diagram displays how to use Multi-cluster kubernetes using A/B deployments ratios to load balance the traffic across two different Kubernetes clusters. The ratio is weighted to 80% to Kubernetes 1.27 cluster and remaining to the 1.28%. F5 BIG-IP as Kubernetes gateway will distribute the traffic to the clusters. This example is using no persistance. However the default persistence is Cookie

Demo on YouTube [video]()

![diagram](https://github.com/mdditt2000/multi-cluster/blob/main/k8s-multi-cluster-ab/diagram/2023-11-17_09-04-51.png)

The link below explain how setup the Calico CNI for the Multi-Cluster Kubernetes environment

* Configuring Calico [clouddocs](https://clouddocs.f5.com/containers/latest/userguide/calico-config.html)
* Lab Guide [lab](https://clouddocs.f5.com/training/community/containers/html/appendix/appendix8/appendix8.html#install-calico)

**Notes**

* BIG-IP needs to add all the peers: the other BIG-IP, our k8s nodes
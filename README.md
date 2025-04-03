Project Overview: Kubernetes Monitoring Dashboard
Objective:
The goal of this project is to create a dashboard in Grafana that helps monitor the health and performance of a Kubernetes cluster. The dashboard will use Prometheus to collect real-time data and display key metrics at different levels: Node, Namespace, Pod, and Container. This will allow users to track resource usage, detect issues, and optimize their cluster efficiently.

What Will the Dashboard Monitor?
The dashboard will be divided into four sections:

Node-Level Monitoring
A Node is a machine (physical or virtual) that runs workloads in the cluster. Here, we will monitor:
The number of Pods running on each node (to track workload distribution).
CPU usage in two ways:

By cores (total CPU usage in cores).
By percentage (how much of the node’s total CPU is being used).

Namespace-Level Monitoring
A Namespace is a logical grouping of resources in Kubernetes (like different environments or teams). Here, we will track:
The number of Pod restarts (to detect failures).
CPU usage (to see how much processing power is used).
Number of running Pods (to check workload size).
Number of Deployments (to see how many application instances are running).
Network traffic (incoming and outgoing data for the namespace).
Memory usage (to track how much RAM is being used).

Pod-Level Monitoring
A Pod is the smallest deployable unit in Kubernetes (it contains one or more containers). We will monitor:
Network traffic (data in and out).
Disk I/O (how much data is being read and written to storage).
CPU usage as a percentage.
Pod age (how long the Pod has been running).
Average memory usage (how much RAM the Pod consumes).

Container-Level Monitoring
A Container is the actual running instance of an application. We will track:
CPU usage (how much processing power the container consumes).
Memory usage (how much RAM the container uses).

Making the Dashboard Interactive
To make the dashboard flexible, we will use variables in Grafana. This means users can easily filter data by:
Node (to see metrics for a specific node).
Namespace (to analyze workloads in a specific environment).
Pod (to check details of a particular application instance).
Container (to inspect individual application components).

Technology Used:
Kubernetes (Kind) – A lightweight Kubernetes cluster for local testing.
Prometheus – A monitoring system to collect metrics.
Grafana – A visualization tool to create the dashboard.
Node Exporter & cAdvisor – Tools for collecting system and container data

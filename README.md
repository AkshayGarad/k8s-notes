# K8s Notes

## 1.  Explain what are some Pods usage patterns?
A pod is the smallest deployable unit in Kubernetes and represents a single instance of a running process in a cluster. Pods can be used in a variety of ways to deploy and manage containerized applications. Here are some common usage patterns for pods:

1. Single-Container Pods: This is the simplest and most common usage pattern for pods, where a single container is deployed in a pod. This pattern is useful for deploying standalone applications, such as web servers, databases, and backend services.

2. Sidecar Pattern: In this pattern, a secondary container (called a sidecar container) is deployed alongside the primary container in the same pod. The sidecar container runs alongside the main container and provides additional functionality, such as logging, monitoring, or security. For example, a sidecar container could collect application logs and forward them to a centralized logging system.

3. Ambassador Pattern: In this pattern, a container is deployed in a pod that acts as a proxy for incoming network traffic. The ambassador container can perform tasks such as load balancing, SSL termination, and authentication, while the main container focuses on application logic. This pattern is useful for deploying microservices that require advanced networking capabilities.

4. Init Container Pattern: In this pattern, an init container is deployed alongside the main container in the same pod. The init container runs before the main container and performs initialization tasks such as configuring the environment or setting up the database. This pattern is useful for ensuring that the main container starts up with the correct environment settings.

5. DaemonSet Pattern: In this pattern, a container is deployed on each node in the cluster using a DaemonSet. The DaemonSet ensures that the container is deployed on every node in the cluster, providing node-local services such as monitoring or logging.

These are just a few of the common usage patterns for pods in Kubernetes. By leveraging these patterns, developers can design and deploy scalable, efficient, and highly available containerized applications.
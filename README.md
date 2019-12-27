# k8s-learning
K8s learning

# PODS:
In Kubernetes, Pods are responsible for running your containers. Every Pod holds at least one container, and controls the execution of that container. When the containers exit, the Pod dies too.

# ReplicaSets:
A ReplicaSet ensures that a set of identically configured Pods are running at the desired replica count. If a Pod drops off, the ReplicaSet brings a new one online as a replacement.

# Secrets:
Secrets are used to store non-public information, such as tokens, certificates, or passwords. Secrets canbe attached to Pods at runtime so that sensitive configuration data can be stored securely in the cluster.

# Deployments:
A Deployment is a higher-order abstraction that controls deploying and maintaining a set of Pods. Behind the scenes, it uses a ReplicaSet to keep the Pods running, but it offers sophisticated logic for deploying, updating, and scaling a set of Pods within a cluster.
- Deployments support rolling update and rollbacks.
- Rollouts can even be paused.

# DaemonSets:
DaemonSets provide a way to ensure that a copy of a Pod is running on every node in the cluster. As a cluster grows and shrinks, the DaemonSet spreads these specially labeled Pods across all of the nodes.
- DaemonSet used to install or configure software on each host node.
Note: A node is a worker machine in Kubernetes, previously known as a minion. A node may be a VM or physical machine, depending on the cluster.

# Ingresses:
Ingresses provide a way to declare that traffic ought to be channeled from the outside of the cluster into destination points within the cluster. One single external Ingress point can accept traffic destined to many different internal services.
- Route Traffic to and from cluster.
- Provide Single ssl endpoints for multiple applications.

# CronJobs:
CronJobs provide a method for scheduling the execution of Pods. They are excellent for running periodic tasks like backups, reports, and automated tests.
- Use common cron syntax to schedule tasks.

# CRDs:
CustomResourceDefinitions, or CRDs, provide an extension mechanism that cluster operators and developers can use to create their own resource types.
- CRD defines new resource type and tells k8s about it.
- Once new resource type is added, new instances of that resource may be created.
- Handling CRD changes is up to you. A common pattern is to create custom controller that watches for new CRD instances and responds   accordingly.

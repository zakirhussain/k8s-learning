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

# 

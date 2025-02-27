Kubernetes Network Policy Explained
A Kubernetes Network Policy is a resource that defines how pods communicate with each other and with other network endpoints. It acts as a firewall at the pod level, allowing or restricting traffic based on rules.

1. Why Use Network Policies?
By default, in Kubernetes:

All pods can communicate with each other, regardless of namespace.
There are no restrictions on inbound or outbound traffic.
Using Network Policies, you can:

Restrict pod-to-pod communication.
Allow or deny traffic based on namespaces, labels, and ports.
Secure applications by implementing least privilege access.
2. Key Components of a Network Policy
A NetworkPolicy resource consists of:

Component	Description
podSelector	Selects the pods to apply the policy to (based on labels).
policyTypes	Specifies whether the policy controls Ingress, Egress, or both.
ingress	Defines allowed inbound traffic rules.
egress	Defines allowed outbound traffic rules.

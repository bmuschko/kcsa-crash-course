# Kubernetes and Cloud Native Security Associate (KCSA) Crash Course

Security is a core principle in software design. Its aim is to keep an application or runtime environment functional and as impenetrable as possible to attacks. The [Kubernetes and Cloud Native Security Associate (KCSA)](https://training.linuxfoundation.org/certification/kubernetes-and-cloud-native-security-associate-kcsa/) teaches the skills and practices for securing a Kubernetes environment.

In this course, trainer Benjamin Muschko will teach you the fundamentals of security for Kubernetes with the focus on helping you to pass the certification exam. We’ll look at common security tools to identify concerns and apply the relevant changes to comply with established practices to harden a Kubernetes cluster and the applications running inside of it.

## Demos

* [Configuring a kube-bench suggestion in the API server](https://learning.oreilly.com/interactive-lab/fixing-issues-discovered/9781098149659/)
* [Enforcing a Pod Security Standard](https://learning.oreilly.com/interactive-lab/creating-a-pod/9781098149871/)
* [Applying security best practices to a Dockerfile](https://learning.oreilly.com/interactive-lab/applying-security-best/9781098149970/)

## Quizzes

**Quiz 1:**

The PCI Security Standards Council (PCI SSC) helps with standardizing what kind of data? (single choice selection)

1. Health information privacy, e.g. through HIPAA.
2. All customer data.
3. Electronic payment data, e.g. credit card information.
4. Data sent between Kubernetes cluster components.

<details><summary>Answer</summary>
<p>
The correct answer is 3. <a href="https://www.pcisecuritystandards.org/about_us/">PCI SSC standards</a> and resources help protect the people, processes, and technologies across the payment ecosystem to help secure payments worldwide.
</p>
</details>

**Quiz 2:**

Select all valid options for deploying etcd on a Kubernetes cluster. (multiple choice selection)

1. On a single control plane node.
2. As a multi-node etcd cluster.
3. Only on a single control plane node.
4. Only in a Pod running on the worker nodes.

<details><summary>Answer</summary>
<p>
The correct answer is 1 and 2. <a href="https://kubernetes.io/docs/tasks/administer-cluster/configure-upgrade-etcd/">Etcd</a> can be deployed on a single control plane for testing purposes. In production, it makes more sense to set up a HA cluster with multiple etcd instances.
</p>
</details>

**Quiz 3:**

Where do you keep client certificates used to communicate with a Kubernetes cluster using `kubectl`? (single choice selection)

1. In the `KUBECONFIG` environment variable.
2. In the values of the `client-certificate-data` and `client-key-data attributes` in the `kubeconfig` file.
3. In the file `$USER_HOME/.kube/certs`.
4. Client certificates do not need to be stored on the machine running `kubectl`.

<details><summary>Answer</summary>
<p>
The correct answer is 2. Every user entry in the <a href="https://kubernetes.io/docs/concepts/configuration/organize-cluster-access-kubeconfig/">kubeconfig file</a> will have to have a base64-encoded value for the client certificate. This information will be sent every time you make a call based on the user selected for the current context.
</p>
</details>

**Quiz 4:**

Configuring audit logging rules with RequestResponse may have an impact on what aspect? (single choice selection)

1. CPU usage on control plane nodes.
2. Data security.
3. Memory usage on worker nodes.
4. Disk space usage on the configured backend.

<details><summary>Answer</summary>
<p>
The correct answer is 4. The <a href="https://kubernetes.io/docs/tasks/debug/debug-cluster/audit/#audit-policy">audit log policy</a> RequestResponse captures the most information possible for incoming requests. Therefore, you will need to make sure you can store the data on the configured backend. CPU and memory will not be impacted significantly by configuring audit logging.
</p>
</details>

**Quiz 5:**

A Network Policy configures an egress rule. What does it configure? (single choice selection)

1. Incoming network traffic to the API server.
2. Outgoing traffic from one Pod to another.
3. TLS termination for Ingresses.
4. Firewall rules to prevent traffic from the internet to the Kubernetes cluster.

<details><summary>Answer</summary>
<p>
The correct answer is 2. <a href="https://kubernetes.io/docs/concepts/services-networking/network-policies/">Network policies</a> control Pod-to-Pod communication. Ingress rules configure incoming network traffic to a Pod. Egress rules configure outgoing traffic from a Pod.
</p>
</details>
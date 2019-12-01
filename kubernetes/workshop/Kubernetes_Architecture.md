## Kubernetes Architecture

- Kubernetes is a sophisticated platform consisting of various components that enables us to run production-ready container applications robustly and reliably. It is crucial to learn about its architecture and design to understand how it works and why it is so successful. Kubernetes is designed to run applications on clusters on the cloud or on-premise systems. Virtual or physical server instances are used with a shared network in these clusters to operate in harmony. This is the actual environment where all Kubernetes components and user applications are configured and run.

- Servers in a Kubernetes cluster are given two essential roles: master or node. If a server is assigned with the master role, it is expected to run centralized logical components of Kubernetes. It is possible to have more than one master server to achieve high availability, and the master servers run the Kubernetes API server, key/value store, scheduler, and controllers. These components create the brain of Kubernetes that interacts with the outside world and makes decisions based on the changes in the cluster or user demands. Other servers in the clusters are assigned the node role to run the workload as containers. Node servers receive the definition of the workload from the master and create, update, or delete the containers accordingly. In addition, nodes form the required networking and storage for the containers and forward the traffic between them.

- Kubernetes with master and node components work on the desired state of applications provided by the Kubernetes API. For example, it is possible to send a declarative JSON or YAML definition of a workload to the Kubernetes API in master servers. Master components enrich these definitions for the required storage, networking, and computing resources and these are then sent to nodes for execution. Node instances execute the plan by running containerized applications and checking application statuses continuously. To sum up, the Kubernetes cluster tries to achieve the desired state, defined in JSON or YAML, by changing and testing the actual state. In the following sections, components in the master and node servers are described in more detail, as
 ![](https://raw.githubusercontent.com/collabnix/dockerlabs/master/kubernetes/workshop/img/KubernetesArchitecture.jpg)
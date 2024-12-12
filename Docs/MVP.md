# MVP

## Control Plane

- **API Server**
- **Scheduler**
- **Simple State Store** (e.g., SQLite)

## Node-Level Components

- **Node Agent**: Executes container commands.
- **Container Runtime**: Integrates with Docker.

## Networking

- **Basic Container-to-Container and External Communication**

## Resiliency

- **Simple Health Checks and Container Restarts**

---

# Target Features

## 1. Core Orchestration Components

### a. Control Plane

The brain of the orchestrator that makes decisions about the cluster state.

- **API Server**:
   - Provides a RESTful interface for clients (users, CLI, UI, or other systems).
   - Receives commands like "deploy a container" or "scale up a service."
   - Validates and processes requests.

- **Scheduler**:
   - Decides where to place containers/pods based on resource availability and scheduling policies (e.g., CPU, memory constraints).
   - Implements scheduling algorithms (round-robin, bin-packing, etc.).

- **State Manager (Controller)**:
   - Monitors the desired vs. actual state of the cluster.
   - Reconciles differences (e.g., reschedules a container if it crashes).
   - Examples:
      - **ReplicaController**: Ensures a specific number of replicas for a service.
      - **NodeController**: Tracks and manages node status.

- **Cluster State Store**:
   - A centralized database to track:
      - Node states (e.g., available resources, health).
      - Container states (e.g., running, stopped, pending).
      - Service configurations and metadata.
   - Examples: etcd (Kubernetes), SQLite (for simpler setups).

### b. Node-Level Components

These are responsible for managing containers on individual machines.

- **Node Agent** (like Kubernetes Kubelet):
   - Runs on every node (physical or virtual).
   - Executes instructions from the control plane (e.g., start/stop containers).
   - Monitors and reports resource usage (CPU, memory, disk, etc.).

- **Container Runtime**:
   - Runs containers on the node.
   - Examples:
      - Docker
      - containerd
      - CRI-O

- **Network Proxy (optional)**:
   - Facilitates communication between containers on the node and the rest of the cluster.
   - May also manage load balancing for services.

---

## 2. Supporting Components

### a. Networking

Ensures communication between containers, services, and nodes.

- **Service Discovery**:
   - Maps service names to IP addresses or DNS records.
   - Allows services to locate each other dynamically.

- **Networking Overlay**:
   - Abstracts networking across multiple nodes to create a unified network.
   - Examples:
      - Flannel
      - Calico
   - Provides:
      - Unique IPs for containers.
      - Connectivity across nodes.

- **Ingress Controller**:
   - Manages external access to services (e.g., HTTP/HTTPS).
   - Routes requests from the outside world to the appropriate service.

### b. Storage

Manages persistent data for containers.

- **Volume Management**:
   - Connects containers to storage volumes (e.g., local disks, cloud storage).
   - Supports dynamic provisioning of storage.

- **Persistent Storage**:
   - Stores data that must persist beyond the lifecycle of a container.
   - Examples:
      - NFS
      - AWS EBS
      - Azure Disks

---

## 3. Observability

Helps monitor and debug the system.

- **Logging**:
   - Collects logs from containers and nodes.
   - Examples:
      - Fluentd
      - Serilog

- **Monitoring**:
   - Tracks metrics like CPU usage, memory consumption, and network I/O.
   - Examples:
      - Prometheus (metrics collection)
      - Grafana (visualization)

- **Tracing**:
   - Tracks requests across multiple services to diagnose performance issues.

---

## 4. Resiliency and Auto-Scaling

Handles failures and adjusts to workloads.

- **Health Checks**:
   - Probes to ensure containers and nodes are running correctly.
   - Types:
      - **Liveness Probe**: Checks if the container is alive.
      - **Readiness Probe**: Checks if the container is ready to serve traffic.

- **Auto-Scaling**:
   - Adjusts the number of running containers or nodes based on demand.
   - Examples:
      - **Horizontal Pod Autoscaling**: Scales based on CPU/memory usage.
      - **Cluster Autoscaler**: Adds/removes nodes.

- **Self-Healing**:
   - Restarts failed containers.
   - Reschedules containers if a node goes down.

---

## 
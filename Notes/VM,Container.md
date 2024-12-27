# Virtual Machine
- A Virtual Machine (VM) is created using virtualization technology, enabling multiple virtual environments to run on a single physical server.
- Traditional physical servers often underutilize resources since only one operating system and application can run at a time.
- To address this issue, the concept of virtualization was introduced using a hypervisor.
- A hypervisor is a software or firmware layer that allows multiple virtual machines to be created by logically isolating hardware resources on a physical server.
- Each virtual machine operates independently, with its own operating system, applications, and resources such as CPU, memory, and storage.
- Virtualization improves resource utilization, cost efficiency, and flexibility, allowing multiple applications to run simultaneously on different virtual machines.

## Why Containers?
- Even with the introduction of virtual machines, resources were still not fully utilized due to the overhead of running a full operating system on each VM.
- Containers were introduced to overcome this limitation by being lightweight and more efficient.

### Key Differences Between Virtual Machines and Containers:

#### Virtual Machines:
- Each VM runs a full operating system, making them resource-intensive.
- Useful for running multiple applications but have significant overhead.

#### Containers:
- Containers do not run a full operating system. Instead, they share the host OS, making them lightweight.
- More efficient in resource utilization compared to VMs.

### Benefits of Containers:
- **Lightweight**: Containers share the host OS, eliminating the need for an additional full OS in each instance.
- **Portability**: Containers package the application along with its dependencies, making it easier to run consistently across environments.
- **Efficiency**: Faster startup times and reduced resource usage compared to virtual machines.

### How Containers Work:
- A container is a self-contained package that includes the application, libraries, and system dependencies required to run the application.
- Containers are created using a base image that includes system dependencies and libraries, providing logical isolation for the application.
- Containers can run on both virtual machines and physical servers, making them highly flexible for deployment.



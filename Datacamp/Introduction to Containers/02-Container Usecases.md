# Container Usecases
Docker is a popular open-source software platform that has revolutionized and standardized the way containers are built, distributed, and run. It provides a robust set of tools for managing the entire lifecycle of containers.

**Docker Architecture Components:**

- Docker Desktop is a desktop application for Mac, Linux, and Windows that provides a graphical user interface (GUI) for managing containers, applications, and images. It also includes the Docker Engine.
- Docker Engine operates as a client-server application.
	- Docker Client users interact with Docker actions primarily through the command-line interface (CLI) or Docker Desktop.
    - Docker Daemon is the core service that runs continuously in the background, responsible for building, running, and managing all Docker objects. It must be running for Docker to function.

| Docker Objects     | Description                                                                                                                                                |
| ------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Dockerfile         | A text file containing a series of instructions (like a recipe) for building a Docker image. It's the blueprint's definition.                              |
| Docker Image       | A read-only template or blueprint created from a Dockerfile. It encapsulates an application and its environment.                                           |
| Docker Container   | A runnable instance of a Docker image. It's an isolated environment where the application executes.Multiple containers can be created from a single image. |
| Docker Registeries | Centralized repositories for storing and managing container images. Docker Hub is a popular public registry.                                               |

---
## Container Orchestration

When applications require multiple containers,container orchestration becomes essential. It is the automated management and coordination of these multiple containers, ensuring they work together effectively and efficiently. An orchestrator is the tool used for this purpose.

- Coordinates large numbers of containers, ensuring they function harmoniously.
- Developers define the desired state in a configuration file and the orchestrator automatically achieves and maintains this setup.
- Adds or removes containers based on demand.
- Dynamically adjusts computing resources for specific containers.
- Automates tasks like resource allocation, saving time, improving productivity, and reducing computing costs. 

>[!NOTE]
>Orchestrators automatically restart or replace failed containers, minimizing downtime and ensuring continuous service delivery.

### Orchestration Usecases

- In a microservices architecture applications can be broken down into smaller, independently scalable services, each in its own container.    
- Handling applications with fluctuating resource requirements or peak usage times.
- Automating Pipelines across data engineering, machine learning, and software development.
---
## Kubernetes

Kubernetes (K8s), originally developed by Google and now open-sourced and maintained by the Cloud Native Computing Foundation, is the leading platform for automating the deployment, scaling, and management of containerized applications. It operates as a distributed system, with components spread across virtual or physical machines, either in the cloud or on-premises.

| Kubernetes Architecture Component | Description                                                                                                                                                                |
| --------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Pod                               | The smallest deployable unit in Kubernetes. It consists of one or more containers that share the same computing resources and operate as a unique application environment. |
| Node                              | A host machine (virtual or physical, cloud or on-premise) that runs one or more pods. Nodes abstract machines, making them easily replaceable.                             |
| Control Plane                     | Manages nodes and pods, intelligently assigning pods to available nodes for efficient resource allocation.                                                                 |
| Cluster                           | A group of interconnected nodes managed by a Control Plane.                                                                                                                |

>[!NOTE]
   While Docker is the preferred platform for developers building and managing individual containers due to its user experience, Kubernetes often uses a lighter container engine for orchestrating large numbers of containers, prioritizing efficiency and scalability.

---

## Dockerfiles

A Dockerfile is a text file that defines the contents and build process for a Docker image. It consists of instructions executed in order.

- Instructions are the building blocks within a Dockerfile (e.g., FROM, COPY, RUN, ENTRYPOINT).    
- Commands are executed via the CLI to manage Docker objects.

```Dockerfile
FROM python3.9-slim
COPY /home/app /home/app
WORKDIR /app
RUN pip install -r requirements.txt

ENTRYPOINT ["python","app.py"]
```

---
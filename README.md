# DevOps
#Docker
 1. What is Docker and Why Use It?
What is Docker?
Docker is an open-source containerization platform that allows you to package applications and all their dependencies into a single unit called a container.

Think of it as a lightweight, portable box where your code, runtime, system tools, libraries, and settings are packed together — ready to run anywhere.

Why use Docker?
Portability: Runs consistently on any environment (dev, test, prod).

Lightweight: Uses fewer resources than virtual machines.

Speed: Faster startup and shutdown than traditional apps.

Scalability: Works perfectly with orchestration tools like Kubernetes.

Isolation: Runs apps in isolated environments to prevent conflicts.

2. Difference Between VM and Container
Feature	Virtual Machines	Containers (Docker)
Virtualization Level	Hardware level	OS level
OS	Each VM has its own OS	Share host OS kernel
Resource Usage	Heavy (CPU, memory, disk)	Lightweight
Boot Time	Minutes	Seconds
Image Size	Large (GBs)	Small (MBs)
Portability	Less portable	Highly portable

Summary:
VM = heavy, isolated, full OS
Container = lightweight, share OS, faster and more efficient

3. Images vs Containers
Aspect	Docker Image	Docker Container
Definition	Blueprint/template for a container	Running instance of an image
Mutable?	No (read-only)	Yes (runtime changes possible)
Stored on	Disk (local or registry like Docker Hub)	Memory/disk while running
Command	docker build, docker pull	docker run, docker start/stop
Example	An image of Nginx	A live Nginx server running from that image

Think of an image like a class in programming, and a container like an object created from that class.

 4. Docker Architecture
 Components of Docker:
1. Docker Engine
The core component installed on your machine.

It runs the Docker Daemon and exposes the Docker API.

2. Docker Daemon (dockerd)
The background process that manages Docker containers and images.

It listens to Docker API requests and executes them (build, run, stop containers).

3. Docker CLI (docker)
Command Line Interface to interact with Docker.

You type commands like docker run, docker ps, etc.

4. Docker Images
Read-only templates used to create containers.

Stored locally or pulled from registries.

5. Docker Containers
Live, running instances of Docker images.

Isolated and include everything needed to run the app.

6. Docker Registries
Repositories to store and share Docker images.

Examples: Docker Hub (public), AWS ECR, GitHub Container Registry (private).

css
Copy
Edit
[You] → [Docker CLI] → [Docker Daemon] → [Containers & Images]
                         ↘
                          [Docker Registry (Docker Hub)]

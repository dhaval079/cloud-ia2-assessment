# Core Algo - Operating System Algorithms Simulator

Welcome to the Core Algo repository! This project aims to provide an interactive platform for simulating various algorithms used in the Operating System subject. The simulator covers four popular algorithms: Round Robin, Banker's Algorithm, Disk Scheduling, and MRU (Most Recently Used). Whether you're a student learning about these algorithms or a professional seeking to refresh your knowledge, Core Algo is designed to cater to all levels of expertise.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
- [Contributors](#contributors)
- [License](#license)

## Introduction

Core Algo provides a user-friendly interface to simulate the behavior of essential Operating System algorithms. This tutorial will guide you through setting up the project using Docker, ensuring easy deployment and scalability.

## Features

Core Algo offers the following key features:

1. **Round Robin Algorithm**: Simulate the round-robin CPU scheduling algorithm with adjustable time quantum.
2. **Banker's Algorithm**: Explore the banker's algorithm for deadlock avoidance and resource allocation.
3. **Disk Scheduling**: Observe disk scheduling algorithms like FCFS, SSTF, SCAN, C-SCAN, LOOK, and C-LOOK in action.
4. **MRU (Most Recently Used)**: Understand the MRU page replacement algorithm and its impact on memory management.

## Technologies Used

- **HTML, CSS, JavaScript**: Frontend development for building the interactive web application.
- **Node.js**: Backend environment for server-side logic.
- **MongoDB**: Database management system for storing simulation data.
- **Docker**: Containerization technology for easy deployment and scalability.
- **CircleCI**: Continuous Integration and Continuous Deployment (CI/CD) pipeline setup for automated testing and deployment.

## Getting Started

## Dockerfile Explanations

This project utilizes multiple Dockerfiles, each serving a specific purpose:

### Dockerfile 1

```
FROM node:15
WORKDIR /app
COPY package.json  .
RUN npm install
COPY . ./
EXPOSE 8000
CMD ["node","index4.js"]
```
Base Image: Starts with the node:15 image, providing a Node.js environment.
Working Directory: Sets /app as the working directory within the container.
Dependencies: Copies package.json and installs dependencies using npm install.
Application Code: Copies the entire application codebase into the container.
Port Exposure: Exposes port 8000 for external access to the application.
Startup Command: Runs node index4.js to start the application.

Dockerfile 2
```
FROM node:15
WORKDIR /app
COPY package.json  .
RUN npm install
RUN npm i nodemon
COPY . ./
EXPOSE 5000
CMD ["node","index1.js"]
```
Similar to Dockerfile 1, but with the following differences:
Installs nodemon for automatic application restarts during development.
Exposes port 5000.
Starts the application using node index1.js.
Dockerfile 3 & 4
These Dockerfiles follow the same structure as Dockerfile 2 but with variations in the exposed ports and entry point files:
Dockerfile 3: Exposes port 5505 and runs node index2.js.
Dockerfile 4: Exposes port 5506 and runs node index3.js.

### Prerequisites

Ensure that you have the following software installed on your system:

- Docker
- Git

### Installation

1. Clone the repository to your local machine:

```
git clone https://github.com/your-username/core-algo.git
cd core-algo
```

2. Build the Docker images:

```
docker-compose build
```
3. Run the Docker containers:
```
docker-compose up
```

Now, you should be able to access the simulator by visiting `http://localhost:3000` in your web browser.

## Usage

Once the simulator is up and running, explore the different algorithms and customize their parameters as needed. Follow the on-screen instructions to interact with the simulations and gain insights into Operating System algorithms.

We welcome contributions from the open-source community. Feel free to submit bug reports, feature requests, or pull requests to help improve Core Algo.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

We hope you find Core Algo helpful and engaging! If you have any questions, please feel free to contact us.

# Inception

## Introduction

The Inception project is part of a system administration series that introduces Docker. The goal is to create a personal virtualized environment comprising various interconnected services, all managed via Docker containers.

## Features

- **Docker Containers**: Each service runs in its isolated Docker container, ensuring clean, reproducible environments.
- **Service Management**: Includes services like NGINX with SSL, WordPress with php-fpm, and a MariaDB database.
- **Data Persistence**: Uses Docker volumes to manage persistent data for WordPress and MariaDB.
- **Custom Docker Networking**: Utilizes Docker networks to facilitate communication between containers.
- **Security Practices**: Implements best practices such as using environment variables for configuration to avoid hard-coded credentials.

## Getting Started

### Prerequisites

- Docker and Docker Compose installed on your machine
- Virtual Machine setup (recommended for isolation and if not sudo permissions are available)

### Installation

1) git clone [repository-url] inception
2) cd inception
3) make all
  
## Configuration

- The project configuration is managed through a `docker-compose.yml` file, which orchestrates the deployment of all services.
- Environment variables are defined in a `.env` file, which should be configured according to personal or production needs.

## Usage

After setting up the containers with `make all`, your services will be up and running. Access the services as configured:

- **NGINX** on HTTPS using the defined domain (e.g., `https://yourdomain.com` configured to point to your VM's IP).

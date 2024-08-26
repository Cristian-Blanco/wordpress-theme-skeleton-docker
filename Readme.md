# WordPress Theme Development Skeleton

Welcome to the WordPress Theme Development Skeleton! This project serves as a boilerplate for creating a WordPress theme, providing a structured architecture and pre-configured .git setup. It includes a docker-compose.yml file for easy project setup and management.

## Table of Contents
- [Project Description](#project-description)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
    - [Introduction](#introduction)
    - [Installation](#installation)

## Project Description
This repository is designed as a skeleton for developing custom WordPress themes. It includes a well-structured architecture with necessary files and configurations to get you started quickly. The included docker-compose.yml file simplifies the installation process, ensuring a smooth setup and execution of your WordPress development environment.

## Prerequisites
Before you begin, ensure you have the following tools installed on your system:

- **Docker:** [Download and Install Docker](https://www.docker.com/get-started)
- **Docker Compose:** [Download and Install Docker Compose](https://docs.docker.com/compose/install/)

Make sure to follow the installation instructions provided on the respective websites to set up Docker and Docker Compose properly on your machine.

docker-compose down --remove-orphans

## Getting Started
### Setting Up the Project
#### Clone the repository:
```bash
git clone https://github.com/Cristian-Blanco/wordpress-theme-skeleton-docker.git
cd wordpress-theme-skeleton
```

#### Run Docker Compose:
Start the Docker containers:
```bash
docker-compose up
```
If you prefer to run the containers in the background (detached mode), use:
```bash
docker-compose up -d
```
This command will build and run the Docker containers, setting up the WordPress environment with the specified theme.

#### Access WordPress

Open your browser and navigate to http://localhost:8020 to access your WordPress site.

### Running the Project

To stop the Docker containers, run:

```bash
docker-compose down
```

### Using npm and Webpack
#### Install npm dependencies
To install necessary npm packages, run:
```bash
docker-compose run npm install
```

#### Build the project with Webpack
To build the theme assets using Webpack, run:
```bash
docker-compose run npm run build
```
For development with automatic file watching, use:

```bash
docker-compose run npm run dev
```

## Configuration
### Configuring Webpack for New Themes
If you create a new theme and want to use the `src` directory with Webpack, you need to configure `webpack.config.js` to point to the new theme.

### Updating Theme Names

If you change the theme name, make sure to update the following:

- **webpack.config.js** - Update paths and output configuration.
- **docker-compose.yml** - Update the volumes to point to the correct theme directory.
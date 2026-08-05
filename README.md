# What is this?

This is a small, PHP Docker stack environment for web app development. It can be used as a lightweight and clean alternative to complete development environments or LAMP solution stack software as XAMPP or AMPPS.

>[!WARNING]
> Keep in Mind
>
> This project is designed to help with learning web development using Docker and is not intended for production use. Moreover, used versions are not dynamic: the project uses the latest stable minor versions of PHP, MySQL and PHPMyAdmin as at 5 August, 2026.

---

# How to use this repository

## Prerequisites

Before you begin, the following software must be installed on your system:

- [Git](https://git-scm.com/install/linux)
- [Docker Engine](https://docs.docker.com/engine/install/)
- [Docker Compose](https://docs.docker.com/compose/install/)

You can check the installation by running `git -v`, `docker -v` and `docker-compose -v`, respectively, in your terminal.

## Setting up the environment
1. Open your terminal and clone this repository:

    ```sh
    git clone https://github.com/wdjacobo/docker-lamp
    ``` 

2. Build and run the containers. Run the following command in the cloned repository directory:

    ```sh
    docker compose up -d
    ```

## Accessing to the server and the database

If everything has gone smoothly, the server would be accesible navigating to [`http://localhost:80`](http://localhost:80) through a web browser.

Also, database management can be done using the PHPMyAdmin software, accesible at [`http://localhost:8080`](http://localhost:8080), or connecting to the database with a client as MySQLWorkbench or DBeaver, through the `3306` port.

## Using the environment for web development

First of all, stop the containers by running `docker compose down` in the cloned repository directory. Then, simply replace the files inside `my_app` folder with your own `.php`, `.html`, `.css` or `.js` files. Run the containers again (remember: `docker compose up -d`) to see your own app runing at [`http://localhost:80`](http://localhost:80).

## Customising this environment

This is a basic environment: possibilies for improvement and customisation are countless. Here are a few of these possibilities:

- Change default used ports. The default ports I established may be in use by other processes in your machine.
- Change default environment variables and add your own.
- Add more containers, e.g., [composer](https://hub.docker.com/_/composer).
- Add container names to the `docker-compose.yaml` file using `container_name: <my_container_name>` for each service.

---

# See also

The following links will lead you to the sources I used as the main references:

- [docker-compose-lamp](https://github.com/sprintcube/docker-compose-lamp) - A much more elaborate and customizable project to keep in mind
- [How to set up a simple LAMP server with DOCKER in 3 minutes](https://medium.com/@mikez_dg/how-to-set-up-a-simple-lamp-server-with-docker-images-in-2023-9b0e24476ec6) - An easy follow along tutorial to build something similar to this repository

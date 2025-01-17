
# Lab 0 - Checkout template project and run Digital.ai Release

## Collect all prerequisites

Check all prerequisites:

* A git client
* A GitHub account
* Docker Desktop

Start Docker.

## Checking out the template project

The Digital.ai Release Integration SDK provides a template project to get started. 

The template project **release-integration-template-python** is located on GitHub:

https://github.com/digital-ai/release-integration-template-python

In this lab we will use the template project directly to make sure you can run Digital.ai Release and run a sample plugin. To build a custom integration, you would create a duplicate of this project. During the workshop, we will do this in Lab 2.

For now, create a copy of the template project on your local machine with the following command

**Https:**

    git clone https://github.com/digital-ai/release-integration-template-python.git

**Private key:**

    git clone git@github.com:digital-ai/release-integration-template-python.git

## Run a development instance of Digital.ai Release

Open a terminal window and launch the development environment with the following commands

    cd release-integration-template-python
    cd dev-environment
    docker compose up -d --build

When the docker command is finished, the containers will still be starting. In Docker Desktop, check the logs of the `dev-environment-digitalai-release-1` container until it displays the following lines:

    2023-04-26 11:48:21 2023-04-26 09:48:21.377 [main] {activemq.broker=embedded-broker} INFO  c.x.x.s.jetty.JettyServerListener - Digital.ai Release has started.
    2023-04-26 11:48:21 2023-04-26 09:48:21.378 [main] {activemq.broker=embedded-broker} INFO  c.x.x.s.jetty.JettyServerListener - You can now point your browser to http://host.docker.internal:5516/

In a browser, go to http://localhost:5516. This should take you to the Digital.ai Release login screen. Log in with username `admin` and password `admin`


---

[Next](lab-1-run-hello-world.md)


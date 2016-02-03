+++
title = "Install Docker"
description = "Getting started with Docker"
keywords = ["beginner, tutorial, Docker"]
[menu.linux]
identifier = "linux_install"
weight = 1
+++

# Install Docker

This installation procedure is written for users who are unfamiliar with package
managers. If you are comfortable with package managers, prefer not to use
`curl`, or have problems installing and want to troubleshoot, please use our
`apt` and `yum` <a href="https://docs.docker.com/engine/installation/"
target="_blank">repositories instead for your installation</a>.

1. Log into your Ubuntu installation as a user with `sudo` privileges.

2. Verify that you have `curl` installed.

        $ which curl

    If `curl` isn't installed, install it after updating your manager:

        $ sudo apt-get update
        $ sudo apt-get install curl 

3. Get the latest Docker package.

        $ curl -fsSL https://get.docker.com/ | sh

    The system prompts you for your `sudo` password. Then, it downloads and
    installs Docker and its dependencies.

    >**Note**: If your company is behind a filtering proxy, you may find that the
    >`apt-key`
    >command fails for the Docker repo during installation. To work around this,
    >add the key directly using the following:
    >
    >       $ curl -fsSL https://get.docker.com/gpg | sudo apt-key add -

4. Verify `docker` is installed correctly.

        $ docker run hello-world
        Unable to find image 'hello-world:latest' locally
        latest: Pulling from library/hello-world
        535020c3e8ad: Pull complete
        af340544ed62: Pull complete
        Digest: sha256:a68868bfe696c00866942e8f5ca39e3e31b79c1e50feaee4ce5e28df2f051d5c
        Status: Downloaded newer image for hello-world:latest

        Hello from Docker.
        This message shows that your installation appears to be working correctly.

        To generate this message, Docker took the following steps:
         1. The Docker Engine CLI client contacted the Docker Engine daemon.
         2. The Docker Engine daemon pulled the "hello-world" image from the Docker Hub.
         3. The Docker Engine daemon created a new container from that image which runs the
            executable that produces the output you are currently reading.
         4. The Docker Engine daemon streamed that output to the Docker Engine CLI client, which sent it
            to your terminal.

        To try something more ambitious, you can run an Ubuntu container with:
         $ docker run -it ubuntu bash

        Share images, automate workflows, and more with a free Docker Hub account:
         https://hub.docker.com

        For more examples and ideas, visit:
         https://docs.docker.com/userguide/


## Where to go next

At this point, you have successfully installed Docker. Leave the terminal
window open. Now, go to the next page to [read a very short introduction Docker
images and containers](step_two.md).


&nbsp;

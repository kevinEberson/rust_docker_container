# rust_docker_container
A Docker container for developing applications in rust independent from the main os, with shared volume.

# Prerequisites
- Docker installed
- Docker extension for Visual Studio Code installed

# Running the container
Running the container is easy; Start by opening the "source" folder in Visual Studio Code. After the workspace finished loading, press: ctrl + shift + P for opening the command palette. In the command palette, select or type "Dev Containers: Reopen in Container". This will build the container, and open it for you when the build is finished. Once the container completes building, you will be automatically changed to */rust*, which is the shared folder.

# Shared folder
The shared folder allows your host pc to connect to you Docker container and transfer file to, or from the container. The main aim for the shared folder is that you can create and develop rust projects while automatically saving any code to your computer. If you delete the container, your projects you made will still be available in the *share* folder. In the *./.devcontainer/devcontainer.json* file, you can see the configuration of the shared folder. The shared folder is located in ${localWorkspaceFolder}/share (the share folder on your host pc) and linked to the /rust directory within the container.

# Adding extra packages
You can add extra packages to the container by adding them to the Dockerfile. For example, but surely not limited to:
```dockerfile
RUN cargo install espup
```

# Issues
If You run into any issues or bugs, feel free to open up an issue documenting the problem and how to recreate it.
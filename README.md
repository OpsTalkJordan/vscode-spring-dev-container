# vscode-spring-dev-container

> This project adds the Spring toolchain to the base JDK11 container definition from Microsoft. It can easily be changed to a different JDK by changing the base image in the Dockerfile.

A **development container** is a running [Docker](https://www.docker.com) container with a well-defined tool/runtime stack and its prerequisites. The Remote - Containers extension in the [Remote Development](https://aka.ms/vscode-remote/download/extension) extension pack allows you to open any folder mounted into or inside a dev container and take advantage of VS Code's full development feature set.

This repository contains a **dev container definition** to help get you up and running with a containerized environment. The definition describes the appropriate container image, runtime arguments for starting the container, and VS Code extensions that should be installed. Providing a container configuration file (`devcontainer.json`) and other needed files that you can drop into any existing folder as a starting point for containerizing your project. (The [vscode-remote-try-*](https://github.com/search?q=org%3Amicrosoft+vscode-remote-try-&type=Repositories) repositories built by Microsoft may also be of interest if you are looking for complete sample projects.)

## Using a definition

To add a dev container definition into and existing project copy the `.devcontainer` and `.vscode` directories into the root of your project. If you are already using [Visual Studio Code](https://code.visualstudio.com/) and don't want to override the contents of and existing `.vscode` folder you should be able to copy just the `.devcontainer` folder and ignore everything else. See the [documentation](https://code.visualstudio.com/docs/remote/containers) for details.

> **Note:** If this is your first time creating a dev container, follow the [getting started steps](https://aka.ms/vscode-remote/containers/getting-started) to configure your machine.

## Sharing a definition in an existing repository

You can share a customized dev container definition for your project by adding the files under `.devcontainer` to source control. Anyone who then opens a local copy of your repo in VS Code will be prompted to reopen the folder in a container, provided they have the [Remote Development](https://aka.ms/vscode-remote/download/extension) extension pack installed.

Your team now has a consistent environment and tool-chain and new contributors or team members can be productive quickly. First-time contributors will require less guidance and there will be fewer issues related to environment setup.

## Sample projects

If you want to try a sample project which already has a dev container, check out one of the following repositories provided by Microsoft:

- [Node Sample](https://github.com/Microsoft/vscode-remote-try-node)
- [Python Sample](https://github.com/Microsoft/vscode-remote-try-python)
- [Go Sample](https://github.com/Microsoft/vscode-remote-try-go)
- [Java Sample](https://github.com/Microsoft/vscode-remote-try-java)
- [.NET Core Sample](https://github.com/Microsoft/vscode-remote-try-dotnetcore)
- [Rust Sample](https://github.com/microsoft/vscode-remote-try-rust)
- [C++ Sample](https://github.com/microsoft/vscode-remote-try-cpp)
- [PHP Sample](https://github.com/microsoft/vscode-remote-try-php)

## Common Questions

### Can I just reuse an existing container image or Docker / Docker Compose configuration?

Yes, if you want to use an existing Dockerfile as a starting point, run **Remote-Containers: Add Development Container Configuration Files...** from the Command Palette (<kbd>F1</kbd>). You'll be prompted to select a Dockerfile or Docker Compose file and customize from there. If you prefer, you can also start up the container and [attach to it](https://aka.ms/vscode-remote/containers/attach).

### What is the goal of `devcontainer.json`?

A `devcontainer.json` file is similar to `launch.json` for debugging, but designed to launch (or attach to) a development container instead. At its simplest, all you need is a `.devcontainer/devcontainer.json` file in your project that references an image, `Dockerfile`, or `docker-compose.yml`, and a few properties. You can [adapt it for use](https://aka.ms/vscode-remote/containers/folder-setup) in a wide variety of situations.

## License

Copyright for portions of this project are held by Microsoft Corporation.
Licensed under the MIT License. See https://go.microsoft.com/fwlink/?linkid=2090316 for license information.

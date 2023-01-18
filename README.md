## Devlop on a remote Docker host

This model only requires that a Docker Engine be running on a remote host that your local Docker CLI can connect to. While using the Remote - SSH extension is easier and doesn't require the Docker CLI to even be installed locally, this model can be useful for situations where you already have a host you are connecting to from the command line. This approach is also useful if you are looking to attach to already running containers on this remote server.

Setting up VS Code to attach to a container on a remote Docker host can be as easy as setting the [Docker extension](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker) docker.environment property in settings.json and restarting VS Code (or reloading the window).

```JSON
{
    "docker.environment": {
        "DOCKER_HOST": "ssh://your-remote-user@your-remote-machine-fqdn-or-ip-here"
    }
}
```

https://code.visualstudio.com/remote/advancedcontainers/develop-remote-host#_connect-using-the-docker-cli


# Sunken Kitchen Challenge

## Project Strucutre

* `config`: configuration files used by applications
* `workloads`: service workloads used by systemd, thse files are also mounted in /etc/containers/systemd
* `src`: your source code

## The Development Environment

### Devcontainer CLI

Simply run:

```shell
devcontainer up --workspace-folder .
```

You need to `--docker-path` if using podman (or something else that is not docker):

```shell
devcontainer up --docker-path=$(which podman) --workspace-folder .
```

### VSCode

* Ensure that the [Remote Development extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack) installed in VSCode.

Devcontainers upstream documentation:
  
  * <https://containers.dev/>
  * https://github.com/devcontainers/cli

You can use the VSCode devcontainer extension to start your containerized development environment.

```shell
cd <absolute/path/to>/maestro-challenge/eclipse-bluechi
code .
```

VSCode detects automatically that a `.devcontainer` folder exists inside this subfolder.
Please confirm the dialog to reopen VSCode inside the devcontainer.
Afterwards, open a new terminal inside the devcontainer in VSCode.

## License

[Apache-2.0](./LICENSE)

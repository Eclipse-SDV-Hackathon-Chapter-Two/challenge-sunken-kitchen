# The Sunken Kitchen Challenge

This challenge is about being creative while using Eclipse SDV projects to provide your own
solution architecture and implementattion.

The only hard requirement is to use at least one [Eclipse SDV project](https://sdv.eclipse.org/projects/).

The challenge provides a basic environment using devcontainers with:

* AutoSD (CentOS Stream 9 Automotive Distribution) as the base OS;
* Systemd + Podman + [Eclipse BlueChi](https://github.com/eclipse-bluechi/bluechi) as the workload orchestration stack;
* [Eclipse uProtocol](https://eclipse-uprotocol.github.io/) as the service mesh spec;
* [Eclipse Kuksa Databroker](https://github.com/eclipse-kuksa/kuksa-databroker) as the automotive messaging databroker;
* Optional Openshift access if needed.

## Basic Acceptance Criteria

* Use at least one [Eclipse SDV project](https://sdv.eclipse.org/projects/);
  * Bonus points if you use 2+ projects together;
* Provide an architecture diagram about your solution;
  * You can get inspired by some of the official [Eclipse SDV Blueprints](https://github.com/eclipse-sdv-blueprints);
* Do not rely on any closed source software.

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

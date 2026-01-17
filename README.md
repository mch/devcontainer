# Personal Devcontainer Template

This is my personal devcontainer set up with the languages and so on that I typically use.

## Getting Started

Install mise: https://mise.jdx.dev/getting-started.html

```shell
devcontainer build --workspace-folder .
devcontainer up --workspace-folder .
```

### Execute a command in the running devcontainer
```shell
devcontainer exec --workspace-folder . zsh
```
There seems to be a bug that prevents `devcontainer --workspace-folder . exec zsh` from working, devcontainer CLI 0.81.1.

## Docker commands
### Find the devcontainer for the current directory
```shell
docker ps --filter "label=devcontainer.local_folder=$(pwd)"
```

### Stop the devcontainer for the current directory
```shell
docker stop $(docker ps --filter "label=devcontainer.local_folder=$(pwd)" -q)
```

### Remove the devcontainer for the current directory
```shell
docker ps -a --filter "label=devcontainer.local_folder=$(pwd)" -q | xargs docker rm
```

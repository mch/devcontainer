# Personal Devcontainer Template

This is my personal devcontainer set up with the languages and so on that I typically use.

## Getting Started

Install mise: https://mise.jdx.dev/getting-started.html

```shell
devcontainer build --workspace-folder .
devcontainer up --workspace-folder .
```

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
docker stop $(docker ps --filter "label=devcontainer.local_folder=$(pwd)" -q) | xargs docker rm
```

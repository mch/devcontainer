# Personal Devcontainer Template

This is my personal devcontainer set up with the languages and so on that I typically use.

## Getting Started

mise is used to install the devcontainer CLI tool and to make it easier to run tasks with it.

Install mise: https://mise.jdx.dev/getting-started.html

Then, build the devcontainer:
```shell
mise run build
```

Start the devcontainer:
```shell
mise run up
```

At this point you should be able to connect to the running devcontainer with editors like VS Code and Zed.

You can also get a shell in the devcontainer:
```shell
mise run zsh
```

Finally, you can stop and remove the container:
```shell
mise run stop
mise run rm
```


# Inspired by https://github.com/devcontainers/images/blob/main/src/universal/.devcontainer/Dockerfile
FROM ubuntu:noble

# Why are we deleting the user 'ubuntu'?
# RUN if id "ubuntu" &>/dev/null; then \
#     echo "Deleting user 'ubuntu' for noble" && userdel -f -r ubuntu || echo "Failed to delete ubuntu user for noble"; \
#     else \
#     echo "User 'ubuntu' does not exist for noble"; \
#     fi

ARG DEBIAN_FRONTEND=noninteractive
RUN apt-get update && \
    apt-get install --no-install-recommends --yes \
        ca-certificates \
        curl

ARG USERNAME=ubuntu

# Persist zsh history in a volume
ENV HISTFILE=/commandhistory/.zsh_history
RUN mkdir /commandhistory \
  && touch /commandhistory/.zsh_history \
  && chown -R $USERNAME /commandhistory

## setup

create docker volume for jetbrains

```bash
docker volume create jetbrains
```

create ssh key for jetbrains gateway

```bash
ssh-keygen -t rsa -b 4096 -C "jetbrains@devcontainer" -f ~/.ssh/jetbrains
```

add mount to devcontainer.json

```json
"mounts": [
    "source=jetbrains,target=/home/vscode/.cache/JetBrains/RemoteDev/dist,type=volume",
    "source=${localEnv:HOME}${localEnv:USERPROFILE}/.ssh/jetbrains.pub,target=/home/vscode/.ssh/authorized_keys,type=bind,consistency=cached,readonly",
]
```

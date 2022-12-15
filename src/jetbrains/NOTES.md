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
    "source=jetbrains,target=${containerEnv:HOME}/.cache/JetBrains/RemoteDev/dist,type=volume",
    "source=${localEnv:HOME}/.ssh/jetbrains.pub,target=${containerEnv:HOME}/.ssh/authorized_keys,type=bind,consistency=cached,readonly",
]
```


# JetBrains (jetbrains)

prepare for jetbrains gateway

## Example Usage

```json
"features": {
    "ghcr.io/Ouvill/devcontainers_features/jetbrains:0": {}
}
```

## Options

| Options Id | Description | Type | Default Value |
|-----|-----|-----|-----|


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


---

_Note: This file was auto-generated from the [devcontainer-feature.json](https://github.com/Ouvill/devcontainers_features/blob/main/src/jetbrains/devcontainer-feature.json).  Add additional notes to a `NOTES.md`._

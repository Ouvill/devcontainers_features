
# JetBrains (jetbrains)

Create an IDE storage location for the jetbrains gateway. Prepare a mount point so that you can mount the `docker volume`.

## Example Usage

```json
"features": {
    "ghcr.io/Ouvill/devcontainers_features/jetbrains:1": {}
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

add mount to devcontainer.json

```json
"mounts": [
    "source=jetbrains,target=/home/vscode/.cache/JetBrains/RemoteDev/dist,type=volume",
]
```


---

_Note: This file was auto-generated from the [devcontainer-feature.json](https://github.com/Ouvill/devcontainers_features/blob/main/src/jetbrains/devcontainer-feature.json).  Add additional notes to a `NOTES.md`._

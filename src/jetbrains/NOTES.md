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

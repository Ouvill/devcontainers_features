
# Authorized Keys (authorized_keys)

copy authorized keys from github account

## Example Usage

```json
"features": {
    "ghcr.io/Ouvill/devcontainers_features/authorized_keys:1": {}
}
```

## Options

| Options Id | Description | Type | Default Value |
|-----|-----|-----|-----|
| github_account | GitHub account name. Enter the account you want to get the public key for | string | - |

## Register SSH key

Register the public key of the specified GitHub account in authorized_keys

If you do not specify an account, just create ~/.ssh folder and exit.

Mount any file to authorized_key.

`.devcontainer.json`

```json
{
    "mounts": [
        "source=${localEnv:HOME}${localEnv:USERPROFILE}/.ssh/id_rsa.pub,target=/home/vscode/.ssh/authorized_keys,type=bind,consistency=cached,readonly"
    ]
}
```


---

_Note: This file was auto-generated from the [devcontainer-feature.json](https://github.com/Ouvill/devcontainers_features/blob/main/src/authorized_keys/devcontainer-feature.json).  Add additional notes to a `NOTES.md`._

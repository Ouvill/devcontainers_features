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

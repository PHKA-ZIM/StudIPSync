# studip-sync

A custom studip-sync fork for windows clients of the PH Karlsruhe.

### Example

```json
{
    "user": {
        "login": "bob42",
        "password": "password"
    },
    "files_destination": "/home/bob/Documents/Uni",
    "media_destination": "/home/bob/Videos/Uni",
    "base_url": "https://studip.uni-goettingen.de"
}

```

The `files_destination` and `media_destination` option are optional. If you omit one of them, the corresponding feature is disabled. You can also specify both options on the commandline. (Using `-d` implies automatically `--full` if no config is present)
If you omit the `login` or `password`, studip-sync will ask for them interactively.

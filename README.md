# studip-sync

A custom studip-sync fork for windows clients of the PH Karlsruhe.

### Example

```json
{
    "user": {
        "login": "[username]",
        "password": "[password]"
    },
    "base_url": "https://lms.ph-karlsruhe.de/studip/index.php?again=yes",
    "auth_type": "general",
    "files_destination": "./data/",
    "media_destination": "./media/"
}


```

The `files_destination` and `media_destination` option are optional. If you omit one of them, the corresponding feature is disabled. You can also specify both options on the commandline. (Using `-d` implies automatically `--full` if no config is present)
If you omit the `login` or `password`, studip-sync will ask for them interactively.


### Changes to studip-sync
To make studip-sync work on windows we had to change a lot.
- robocopy instead of rsync
- chunking file writes from requests instead of binary write of the whole file
- ignore deletion errors
- file paths that are > 280 characters long had to be dealt with

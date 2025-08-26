# BITWARDEN DUPLICATE REMOVAL

Remove duplicates from your Bitwarden vault without exporting your passwords to any file, avoiding loss or theft, and using only the official Bitwarden CLI.

This script does not store any data, nor does it share it with any third party, you can verify this by inspecting the code.

## Install Bitwarden official CLI tool
### Ubuntu

```bash
snap install bw
```

### Other linux distros

Go to [official repo cli](https://github.com/bitwarden/cli/releases)

Download `bw-linux-1.22.1.zip`

```bash
unzip bw-linux-1.22.1.zip
```

If you want to use it from now on, move it to somewhere on your PATH
```bash
sudo mv bw /usr/local/bin/
```

Make it executable

```bash
sudo chmod +x /usr/local/bin/bw
```

## Login and sync

```bash
$ bw login

<you should receive a session key>

$ export BW_SESSION="<session_key>"

$ bw sync
```

## Remove duplicates

```bash
$ chmod +x ./bitwarden-remove-duplicates

$ ./bitwarden-remove-duplicates

Checking Bitwarden session...
To delete:
Amazon | xxxxx@gmail.com | 6GH********
Google | xxxxx@gmail.com | aLX********
Type 'continue' to proceed with deletion:
continue
[i] Deleting item with ID: 4ab1f3b2-4901-xxxx-xxxx-xxxxxxxxxxx
[i] Deleting item with ID: 799d01fd-ce69-xxxx-xxxx-xxxxxxxxxxx
```

## Custom deletion

The script works linking `name`, `username` and `password`.

If you want the script to consider other parameters in order to be considered a "duplicate", feel free to edit that on lines [20-22] of the script.
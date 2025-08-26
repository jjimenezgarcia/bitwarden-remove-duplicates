# BITWARDEN DUPLICATE REMOVAL

## Install Bitwarden official CLI tool
### Ubuntu

```bash
snap install bw
```

### Other linux distros

Go to [official repo cli](https://github.com/bitwarden/cli/releases)

Decompress `tar -xvzf bw-linux-<ARCH>.tar.gz`

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

## Migrate

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
# discord-apt-repo

This repository is to provide an APT repository for Discord deb packages.

## How to install Discord

Tested on:

- Linux Mint 22 / Ubuntu 24.04 LTS

Import the GPG key:

```shell
curl -s https://quoonel.github.io/discord-apt-repo/discord-repo.gpg | sudo gpg --dearmor -o /etc/apt/trusted.gpg.d/discord-repo.gpg
```

Add the APT repository:

```shell
echo "deb [signed-by=/etc/apt/trusted.gpg.d/discord-repo.gpg] https://quoonel.github.io/discord-apt-repo/ stable main" | sudo tee -a /etc/apt/sources.list.d/discord-repo.list
```

Install Discord:

```shell
apt update
apt install discord
```

ℹ️ When APT udpates the `discord` package, it closes automatically the Discord app. You must relaunch it manually.

<p align="center">
    <img src="./.github/steamdeck.png"/>
</p>

<h1 align="center">
Steam Deck Config
</h1>

<p align="center">
My Steam Deck config and customization.
</p>

# Preparation
Mostly, we configures our Steam Deck in `Desktop Mode`, so I highly recommend you connect your device with: 
a `USB Hub` , then connect your `mouse` and `keyboard` . 

If you don't have a `USB Hub`, using buttons and touchpad is still Ok.

This is a part of key mappings.

| Button  | Desktop            |
| -       | -                  |
|   R2    |  Mouse Left Click  |
|   L2    |  Mouse Right Click |
|  Right Touchpad | Mouse Move |
| STEAM + X | Call Keyboard    |

By this way, you can directly control your device in `Desktop Mode`, but it's a little bit `inconvenient`.

# Environment

## Do it first!

### Add password to current user.
In `Desktop Mode`, open `Konsole`, and `add a password` to current user, for sudo use.

```shell
passwd

# New password: 
# Your input will not appear, please make sure your input is correct, then push ENTER.
```

### Disable `steamdeck-readonly`
```shell
# disable
sudo steamos-readonly disable

# enable(if you want to enable it again after config.)
sudo steamos-readonly enable
```


## Flatpak
For `most users`, you can skip this part. This part is for users who have trouble searching apps in `Discover`, mainly for `users in China`.

If your `Discover` searching has no response, please `change the remote mirror`.

```shell
# This will overwrite the official mirror link.
sudo flatpak remote-modify flathub --url=https://mirror.sjtu.edu.cn/flathub

# If you don't want to overwrite, you can add a mirror link.
sudo flatpak remote-add flathub https://mirror.sjtu.edu.cn/flathub/flathub.flatpakrepo
```
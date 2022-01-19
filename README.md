# portmaster-runit

## Description

AUR package letting you use the great [portmaster](https://safing.io/portmaster) on runit systems

## Installation

### Note:

Installing from the AUR is not yet available, and so does the *Lazy Installation*

#### Source install

Clone the repo:

`git clone https://github.com/0x454d505459/portmaster-runit`

Use `makepkg` to create and install the package

`cd portmater-runit`

`makepkg -si`

#### AUR installation (doesn't work right now)

Just install from the [AUR](https://aur.archlinux.org/) with your favourite helper:

`paru -S portmaster-runit`

#### Service linking

After installation is done you need to link the service for it to be `enabled`

`sudo ln -s /etc/runit/sv/portmaster /run/runit/service/portmaster`

#### Starting the service

When the service as been enabled, we now need to starts it:
`sudo sv up portmaster`

#### Finishing

You can now start the portmaster app

## Lasy installation

Just copy paste that script into your terminal

```bash
bash -c "paru -S portmaster-runit && sudo bash -c 'ln -s /etc/runit/sv/portmaster /run/runit/service/portmaster && sv up portmaster'"
```

You may need to replace `paru` with you current AUR helper

# bluetoothctl
Just the bluetoothctl program from bluez-utils, avoiding the ridiculous amount of baggage.

## Steps

Find latest version and hash:
```
$ sudo pacman -Sy
$ pacman -Ss bluez-utils
extra/bluez-utils 5.77-1
    Development and debugging utilities for the bluetooth protocol stack

$ curl -sL https://archlinux.org/packages/extra/x86_64/bluez-utils/download/ | sha256sum
4ac0dfda19390dcbc0c8321cfc52b6068fd984f8299c53c322bcbca306b36673  -
```

Edit PKGBUILD with above vals.

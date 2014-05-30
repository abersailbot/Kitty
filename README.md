kitty-provisioner
=================

Confiure a raspbian image with for use inside kitty.

This sets up networking to act as an access point, installs [config
files](https://github.com/kragniz/dot-files) and sets up udev rules for the GPS
and wind sensor.

With this configuration, the gps appears on `/dev/gps`, the RO Wind on
`/dev/rowind` and the Arduino on `/dev/arduino`.

Installing
----------

Do the following:

```bash
$ git clone https://github.com/abersailbot/kitty-provisioner.git
$ cd kitty-provisioner
```

Edit [`password`](password) and change the password, then run

```bash
$ sudo ./provision
```

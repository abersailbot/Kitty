<<<<<<< HEAD
kitty-arduino
=============

Code to run on kitty's arduino.

Depends on [CMPS10](https://github.com/kragniz/CMPS10) to interact with the
compass.
=======
kitty-provisioner
=================

Confiure a raspbian image with for use inside kitty.

This sets up networking to act as an access point, installs [config
files](https://github.com/kragniz/dot-files) and sets up udev rules for the GPS
and wind sensor.

With this configuration, the gps appears on `/dev/gps`, the RO Wind on
`/dev/rowind` and the Arduino on `/dev/arduino`.
>>>>>>> master-holderarduino

Installing
----------

<<<<<<< HEAD
```bash
$ git clone https://github.com/abersailbot/kitty-arduino.git
$ cd kitty-arduino
$ git submodule init
$ git submodule update
```

Now, if ino tool is installed correctly (if you're using
[kitty-provisioner](https://github.com/abersailbot/kitty-provisioner) this is
done for you), you can compile with:

```bash
$ ino build
$ ino upload
```

Alternately, use make for all the previous steps:

```bash
$ make install
```

Licence
-------

This program is free software: you can redistribute it and/or modify it under
the terms of the GNU General Public License as published by the Free Software
Foundation, either version 3 of the License, or (at your option) any later
version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY
WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A
PARTICULAR PURPOSE.  See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with
this program.  If not, see <http://www.gnu.org/licenses/>.
=======
Do the following:

```bash
$ git clone https://github.com/abersailbot/kitty-provisioner.git
$ cd kitty-provisioner
```

Edit [`password`](password) and change the password, then run

```bash
$ sudo ./provision
```
>>>>>>> master-holderarduino

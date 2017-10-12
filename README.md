Hull
----

These are the files used in the construction of the hull.

`hull.igs` was created by [Paul
Miller](http://www.usna.edu/Users/naome/phmiller/), and is public domain.

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

sails
=====

Kitty's sails, made using [Sailcut](http://www.sailcut.com/). Currently two sails planned:

  * `heavy_air.saildef` - for heavy winds
  * `light_air.saildef` - for light winds

The sails wrap around the mast, so add an extra 83mm (circumference of the mast)
+ 40mm (leech hem) from the mast edge of the sail.

Output formats for printing are stored in [output](output).

kitty-hardware [![Creative Commons Attribution 4.0 International License](http://i.creativecommons.org/l/by/4.0/88x31.png)](http://creativecommons.org/licenses/by/4.0/)
===================================================================================================================================================================

Files relating to Kitty's hardware

This currently contains:

  * [Sails](sails) - Files for the sails
  * [Hull](hull) - Files used in the construction of the hull

![kitty](https://raw.githubusercontent.com/abersailbot/kitty-cad/master/kitty.png)

Unless specified otherwise, the files contained within are licenced under [CC BY
4.0](http://creativecommons.org/licenses/by/4.0/). See [COPYING](COPYING) for
the full licence.

Weights:
  * Boat with most of the stuff in - 13 kilos
  * Keel - 15 kilos

  * box:
    * base > 29 kilos
    * lid 19 kilos
    * 2.09m x 0.72m x 0.60m

    Electorics
    ==========


    Box connectors
    --------------

    ###Plug 1
      1. Rudder Power (7.2v)
      2. Rudder Ground
      3. Rudder Servo Data
      4.
      5.
      6. Multiplexor Power (6v)
      7. Sail Winch Ground
      8. Sail Winch Live (7.2v)
      9. Sail Winch Data
      10.
      11. Multiplexor Ground
      12.

    ###Plug 2
      1. Wifi Ground
      2. Wifi Data-
      3. Wifi Data+
      4. Wifi Power (5v)
      5.
      6. Compass SDA
      7. Compass Ground
      8. Rowind Data
      9. Rowind Ground
      10. Rowind Power (14.4v)
      11. Compass SCL
      12. Compass Power (5v)

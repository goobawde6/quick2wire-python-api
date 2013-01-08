Quick2Wire Python API
=====================

A Python library for controlling the hardware attached to the
Raspberry Pi's header pins, [without running as the root user](http://quick2wire.com/articles/working-safely-with-your-pi/).

STOP PRESS
----------

We have discovered that the Quick2Wire I2C API does not work if you upgrade the kernel of the official Raspbian distribution to Linux 3.6 by running rpi-update.  We are investigating the issue and hope to have a fix soon.  Until then, use the kernel that is distributed with the official Raspbian distro (currently 3.2.27).


Dependencies
------------

The library depends on Python 3. To install Python 3 run this command from an administrator account, such as `pi`:

    sudo apt-get install python3

You'll also find the python tools [virtualenv](http://www.virtualenv.org/en/latest/index.html) and [pip](http://www.pip-installer.org/en/latest/index.html) useful:

    sudo apt-get install python-pip
    sudo apt-get install python-virtualenv


The GPIO API depends on Quick2Wire GPIO Admin.  To install Quick2Wire
GPIO Admin, follow the instructions at
http://github.com/quick2wire/quick2wire-gpio-admin

The I2C and SPI API depend on support in the kernel. Recent raspbian kernels should be fine.


Installation
------------

The library is currently under active development, so we do not
recommend installing it into the system-wide Python libraries. 
Instead, you can either use it without installation or 
install it into an isolated Python development environment created with [`virtualenv`](http://www.virtualenv.org/).

To use the library without installation, add the full path of the
`src` subdirectory of the source tree to the `PYTHONPATH` environment
variable. For example:

    export QUICK2WIRE_API_HOME=[the directory cloned from Git or unpacked from the source archive]
    export PYTHONPATH=$PYTHONPATH:$QUICK2WIRE_API_HOME/src

If you're using virtualenv, make your virtualenv [active](http://www.virtualenv.org/en/latest/index.html#activate-script), and then run:

    python3 setup.py install

Getting Started
---------------

 * [Getting Started with GPIO](http://github.com/quick2wire/quick2wire-python-api/blob/master/doc/getting-started-with-gpio.md)
 * [Getting Started with I2C](http://github.com/quick2wire/quick2wire-python-api/blob/master/doc/getting-started-with-i2c.md)

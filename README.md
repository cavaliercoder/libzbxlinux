# libzbxlinux

This project provides comprehensive monitoring of the Linux kernel using a
natively compiled Zabbix agent module, written in C.

A preconfigured Zabbix Template is also included for your convenience.

Sources in this project are used to compile `libzbxlinux.so` which may be
loaded by a Zabbix agent using the `LoadModule` directive. 

__WARNING__
This project is not yet stable and subject to frequent breaking changes.


## Installation

To compile the agent module the following items are required:

* GNU build tools (`make`, `gcc`, `autoconf`, `automake`, `libtool`, `m4`, etc.)
* [Zabbix sources](http://www.zabbix.com/download.php)

If you are building from sources cloned from GitHub, you first need to
regenerate the build scripts using `./autogen.sh`. Otherwise:

    ./configure --with-zabbix=/usr/src/zabbix/include
    make
    make install

Module file `libzbxlinux.so` will then be installed in `/usr/local/lib`.


## License

libzbxlinux - A Linux kernel extension module for Zabbix
Copyright (C) 2016 - Ryan Armstrong <ryan@cavaliercoder.com>

This program is free software; you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation; either version 2 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program; if not, write to the Free Software
Foundation, Inc., 51 Franklin Street, Fifth Floor, Boston, MA  02110-1301, USA.

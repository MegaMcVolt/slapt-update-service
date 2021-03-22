Slapt update service
--------------------

Copyright (C) 2003-2020 Jason Woodward <woodwardj at jaos dot org>

This program is free software; you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation; either version 3 of the License, or
any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU Library General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program; if not, write to the Free Software
Foundation, Inc., 59 Temple Place - Suite 330, Boston, MA 02111-1307, USA.

**About:**

  Slapt update service is a DBus service which notifies about package updates
  available via slapt-get and gslapt. Slapt update service places an icon in
  the user's notification area when updates are available. Clicking the icon
  starts upgrading with gslapt.

**How it looks:**

![Screenshot](Screenshot.png)

**Requirements:**

  To build from source, you must have these packages mentioned in slack-required
  installed.

**Building and installing:**

  You can install via meson or autotools (deprecated).

 - Meson
    > ```sh
    > meson setup build       # or any dir of your choosing
    > meson compile -C build  # or `ninja -C build` for older meson releases
    > meson install -C build  # or `ninja -C build install` for older meson releases
    > ```
    >> 
    >> Meson/ninja supports `DESTDIR=/path meson install -C build`
    >>
    >> **TIP:**
    >> slapt-update-service.Slackbuild will create a Slackware package.
    >> Run with sudo or as a privileged user.

 - Autotools (deprecated)
    > ```sh
    > ./autogen.sh  # if building from git
    > ./configure
    > make
    > make install  # as privileged user
    > ```
    >>
    >> The Makefile honors DESTDIR.
    >>
    >> **TIP:**
    >> `make pkg` (as privileged user) will create a Slackware package.

## Peter's Exquisite Makefile Collection

A FreeBSD port overlay that contains makefiles for my open-source projects.

### setup

```
git clone https://github.com/rodan/freebsd-overlay.git
echo 'OVERLAYS=FOO/freebsd-overlay' >> /etc/make.conf
```

installing a port is just a 'make' away:

```
cd freebsd-overlay/foo/bar
make install
```
FreeBSD actually creates a package in the background and installs it to the live filesystem, thus all 'pkg'-related commands can be run against the port.

### highlights

package | details
--- | ---
[games/mcarpet2](https://github.com/rodan/magic_carpet_2) | recode of Buffrog's Magic Carpet 2 game now with OpenAL-based directional sounds and support for modern controllers and joysticks
[media-gfx/thpp](https://github.com/rodan/thpp) | thermal processing panel - viewer and analyzer of infrared images compatible with FLIR and IRTIS cameras
[sys-process/daemontools-scripts](https://github.com/rodan/daemontools-scripts) | Scripts for daemontools's supervisor

### see also

in case you were looking for 'Peter's Exquisite Ebuild Collection', which is my Gentoo Linux overlay it's located [here](https://github.com/rodan/overlay).


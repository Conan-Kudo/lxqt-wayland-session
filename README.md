# lxqt-wayland
Files needed for the LXQt Wayland Session: wayland session start script, its desktop entry for
display managers and default configurations for actually supported compositors which are:

* Labwc
* Wayfire
* kwin_wayland
* Sway
* Hyprland

At startup default configuration files for compositors will be copied to `$XDG_CONFIG_HOME/lxqt/wayland` directory
if not existing.

### Compiling source code

Runtime dependencies are [liblxqt](https://github.com/lxqt/liblxqt)and [lxqt-session](https://github.com/lxqt/lxqt-session).
Additional build dependencies are CMake and optionally Git to pull latest VCS checkouts.

Code configuration is handled by CMake. CMake variable `CMAKE_INSTALL_PREFIX` has to be set
to `/usr` on most operating systems.  

To build run `make`, to install `make install` which accepts variable `DESTDIR` as usual.  

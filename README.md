# FullPageOS (7egend version)

This is a fork from https://github.com/guysoft/FullPageOS.

Original README file can be found [here](README.rst)

## Build (docker)

1. Download base OS
  ```sh
  cd src/image
  wget -c --trust-server-names 'https://downloads.raspberrypi.org/raspios_lite_armhf_latest'
  ```

2. Run the container for building
  ```sh
  cd src
  docker run --rm -v `pwd`:/distro --device /dev/loop-control --privileged guysoft/custompios:devel build
  ```

Your image will be available in `src/workspace`.

## Changes to the original version
### Added
- Added7egend splash image
- X11VNC server without password
### Updated
- Chromium to the latest version
### Removed/Disabled
- Camera driver
- Usage statistics
- FullPageOS Dashboard
- FullPageOS Welcome page
- LIGHTTPD service
# CMake Documentation
This folder contains documentation about CMake.

To go back to main page: [Sw Dev Documentation Main Page](README.md)

## Table of Contents
- [Upgrading/Updating CMake](#updatingupgrading-cmake)
- [Selecting which CMake version to use](#selecting-which-cmake-version-to-use)

### Updating/Upgrading CMake

Resources:
- [Medium Article](https://medium.com/@yulin_li/how-to-update-cmake-on-ubuntu-9602521deecb)

Information:
- DO NOT remove/purge the default installed CMake version (which usually comes with ROS).
- Install newer CMake version as written in the linked article.

### Selecting which CMake version to use
You can select the specific CMake version to use by pre-appending the path to that version to the PATH variable. To do that:

    $ PATH="/path/to/cmake/bin:$PATH"  # Example: PATH="/usr/bin:$PATH"
    $ export PATH

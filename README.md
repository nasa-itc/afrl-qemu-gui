# JSTAR AFRL QEMU GUI
A GUI written in Python meant to simplify [QEMU](https://github.com/qemu/qemu) setup and usage.

## Development

Ensure your system has the following dependencies:
- python3
- pip3
- libguestfs-dev

To setup and test the GUI in a Python virtual environment in development/editable mode simply run the
commands below:

```
python3 -m venv venv 
source ./venv/bin/activate
pip3 install -e .
pip3 install https://download.libguestfs.org/python/guestfs-1.40.2.tar.gz
afrl_gui
```

In order to create a release package installable via pip, execute the following command:

```
python3 setup.py sdist --formats=gztar,zip
```

Alternatively, you can use the provided startup script to create the development environment
automatically and run the GUI.

```
sh ./startup.sh
```

## Release

The release can be installed via the generated package in a Python virtual environment using the following
commands:

```
python3 -m venv venv 
source ./venv/bin/activate
pip3 install ./afrl_gui-<VERSION>.tar.gz
```


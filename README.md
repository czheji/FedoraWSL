# FedoraWSL
Fedora on WSL (Windows 10 FCU or later)
based on [wsldl](https://github.com/yuk7/wsldl)

![screenshot](https://github.com/czheji/FedoraWSL/raw/master/img/screenshot.png)

[![CircleCI](https://circleci.com/gh/yosukes-dev/FedoraWSL.svg?style=svg)](https://circleci.com/gh/yosukes-dev/FedoraWSL2)
[![Github All Releases](https://img.shields.io/github/downloads/yosukes-dev/FedoraWSL/total.svg?style=flat-square)](https://github.com/yosukes-dev/FedoraWSL/releases)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)
![License](https://img.shields.io/github/license/yosukes-dev/FedoraWSL.svg?style=flat-square)

### [Download](https://github.com/yosukes-dev/FedoraWSL/releases)


## Requirements
* Windows 10 Fall Creators Update x64 or later.
* Windows Subsystem for Linux feature is enabled.

## Install
#### 1. [Download](https://github.com/yosukes-dev/FedoraWSL/releases) installer zip

#### 2. Extract all files in zip file to same directory

#### 3.Run Fedora.exe to Extract rootfs and Register to WSL
Exe filename is using to the instance name to register.
If you rename it you can register with a diffrent name and have multiple installs.

## (Option)
If you want to use WSL2, convert it with the following command.
```dos
wsl --set-version Fedora 2
```

## How-to-Use(for Installed Instance)
#### exe Usage
```dos
Usage :
    <no args>
      - Open a new shell with your default settings.

    run <command line>
      - Run the given command line in that distro. Inherit current directory.

    runp <command line (includes windows path)>
      - Run the path translated command line in that distro.

    config [setting [value]]
      - `--default-user <user>`: Set the default user for this distro to <user>
      - `--default-uid <uid>`: Set the default user uid for this distro to <uid>
      - `--append-path <on|off>`: Switch of Append Windows PATH to $PATH
      - `--mount-drive <on|off>`: Switch of Mount drives

    get [setting]
      - `--default-uid`: Get the default user uid in this distro
      - `--append-path`: Get on/off status of Append Windows PATH to $PATH
      - `--mount-drive`: Get on/off status of Mount drives
      - `--lxguid`: Get WSL GUID key for this distro

    backup [contents]
      - `--tgz`: Output backup.tar.gz to the current directory using tar command
      - `--reg`: Output settings registry file to the current directory

    clean
      - Uninstall the distro.

    help
      - Print this usage message.
```


#### How to uninstall instance
```dos
>Fedora.exe clean

```

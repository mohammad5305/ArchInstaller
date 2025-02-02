<!-- DevOps.nvim -->
# Arch Linux Installer

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![Telegram][telegram-shield]][telegram-url]

<!-- GETTING STARTED -->
## Introduction

Install archlinux and config based on a yaml configuration

## Getting Started

### Prerequrments

* Just Learning yaml :)


### Installation
First of all we need to install requirements

```sh
pip install pyyaml requests
```

Then we can clone this template or download script directly

```sh
wget archinstaller.ml -O FakeInstaller
# or git clone https://github.com/FakeSudo/ArchInstaller
chmod +x FakeInstaller
./FakeInstaller
```

NOTE: before running Installer write config.yaml or pass a pastbin or git gist url to script

## Configuration

Config will separate into user settings that run after Installation and root settings

### Root settings:

* account
    
    Involves username and password, rootpassword

* hostname

* locale
    
    common: `en_US.UTF-8 UTF-8`

* timezone
    
    Find your timezone with `timedatectl list-timezones`

* shell
    
    Default user shell

    common: `/bin/bash`

* drive
    * blk
        
        The hard drive you want to install arch on it

        example: `/dev/sda`

    * erase
        
        Format the hard drive don't enable this field unless you know what are you doing
        
        example: Boolean value

    * partitions
    
        List of partition to create
        Contains: 

        * size
            
            in `K/M/G` format
                
        * filesystem
                
            type of the partition

            commons: `uefi/linux/swap`

        * number

            the number of the primary partition

    for more information read `fdisk` manual


* bootloader

    Id is the label that your bios will display for your archlinux install and target stand for bios version `UEFI` or `LEGACY`

    common:
    ```
    id: grub
    target: x86_64-efi or i386 for LEGACY
    ```

* base packages

    Packages needed for booting the system

* base daemons

### User settings contains:

* custom script

* aurhelper

    common: `yay/paru`

* user packages

* user daemon



Note: if you configured user setting you should rerun installer command after reboot

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/FakeSudo/DevOps.nvim?style=for-the-badge
[contributors-url]: https://github.com/FakeSudo/DevOps.nvim/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/FakeSudo/DevOps.nvim?style=for-the-badge
[forks-url]: https://github.com/FakeSudo/DevOps.nvim/network/members
[stars-shield]: https://img.shields.io/github/stars/FakeSudo/DevOps.nvim?style=for-the-badge
[stars-url]: https://github.com/FakeSudo/DevOps.nvim/stargazers
[issues-shield]: https://img.shields.io/github/issues/FakeSudo/DevOps.nvim?style=for-the-badge
[issues-url]: https://github.com/FakeSudo/DevOps.nvim/issues
[license-shield]: https://img.shields.io/github/license/FakeSudo/DevOps.nvim?style=for-the-badge
[license-url]: https://github.com/FakeSudo/DevOps.nvim/blob/main/LICENSE.md
[telegram-shield]: https://img.shields.io/badge/Telegram-blue.svg?style=for-the-badge&logo=telegram
[telegram-url]: https://t.me/FakeSudo


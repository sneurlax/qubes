# Qubes 4.0
## Hardware
### Purism laptops

[Upgrade Coreboot before installing Qubes 4.0](https://forums.puri.sm/t/building-coreboot-from-source-official-script/1264):
 
```bash
wget https://code.puri.sm/kakaroto/coreboot-files/raw/master/build_coreboot.sh -
chmod +x ./build_coreboot.sh
sudo ./build_coreboot.sh
```

#### Known issues
##### Librem 13

 - [Keyboard layout issue with `\`/`|` (backslash/pipe) key](https://forums.puri.sm/t/keyboard-layout-unable-to-recognize-pipe/2022/33)
 
    Solution: `xmodmap -e "keycode 94 = backslash bar"` in `dom0` and/or Template/AppVMs

## Configuration

 - [Enable USB keyboard](https://www.qubes-os.org/doc/usb/#how-to-use-a-usb-keyboard)
 
    ```bash
    sudo qubes-dom0-update
    sudo qubesctl state.sls qvm.usb-keyboard
    ```

## Software
### [KDE Plasma](https://www.qubes-os.org/doc/kde/)

Start the process of switching to KDE by using:

```bash
sudo qubes-dom0-update @kde-desktop-qubes
```

but **make sure** to complete the process overviewed [in the installation section of the article above](https://www.qubes-os.org/doc/kde/#installation)

### Core packages

 - konsole
 - konqueror
 - kcalc
 - wget
 - dtrx

*Oneliner (with dependencies for Bitcoin and Monero:*

```bash
sudo apt-get update && sudo apt-get install -y konsole konqueror kcalc dtrx vlc kdenlive wget curl build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils python3  sudo apt-get install libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev libboost-all-dev libqt5gui5 libqt5core5a libqt5dbus5 qttools5-dev qttools5-dev-tools libprotobuf-dev protobuf-compiler libzmq3-dev libunbound-dev libsodium-dev libminiupnpc-dev libunwind8-de liblzma-dev libreadline6-dev libldns-dev libexpat1-dev libgtest-dev doxygen graphviz
```

### *Other*

 - [libreoffice](https://www.libreoffice.org/download/download/)
 - chrome
 - firefox
 - vlc
 - kdenlive
 
 - [sublime-text](https://www.sublimetext.com/3)
 - [keepassxc](https://keepassxc.org/download/)
 - [veracrypt](https://www.veracrypt.fr/en/Downloads.html)
 - [riot-web](https://riot.im/desktop.html)
 
 - [torguard](https://torguard.net/downloads.php)
 - [mullvad](https://mullvad.net/en/download/)
 - [airvpn](https://airvpn.org/linux/)
 
 ## Templates
 
  - [Fedora Minimal](https://www.qubes-os.org/doc/templates/fedora-minimal/)
  - [Debian](https://www.qubes-os.org/doc/templates/debian/)
  - [Ubuntu](https://www.qubes-os.org/doc/templates/ubuntu/)
  - [Archlinux](https://www.qubes-os.org/doc/templates/archlinux/)
 
 ## Resources
 
 - [Qubes cheatsheet](https://github.com/Jeeppler/qubes-cheatsheet) 

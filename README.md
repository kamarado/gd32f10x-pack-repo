# GigaDevice GD32F10x CMSIS Pack Repository

This repository contains an unofficial GigaDevice GD32F10x CMSIS Pack for [GNU MCU Eclipse][packs-manager].

Based on [Milandr MCU 1986x CMSIS Pack Repository](https://github.com/in4lio/mdr1986x-pack-repo)

### How to install the package (Eclipse)

- [Add][packs-manager-config] Milandr MCU repository, specifying the path to [_"index.pidx"_][index.pidx]
file:
```
Eclipse Menu → Window → Preferences → C/C++ → Packages → Repositories → Add...

Type       CMSIS Pack
Name       GigaDevice GD32F10x
URL        https://github.com/kamarado/gd32f10x-pack-repo/raw/main/index.pidx
```
With old versions of Packs Manager, you should use [_"index.idx"_][index.idx] file.

- [Open][packs-manager-persp] the Packs perspective and [install][packs-manager-install] `GD32F10x`
package from `GigaDevice` group.

- The path to the packages is defined in `packs_path` macro, but for the plug-in version that I use,
this macro is not visible from tools configurations. Therefore, you may also need to set `packs_path`
macro manually:
```
Eclipse Menu → Window → Preferences → Run/Debug → String Substitution → New...

Name       packs_path
Value      <path to packages>
```

### How to examine/modify the peripheral registers (Eclipse)

[The peripherals registers view][debug-registers]

### How to rebuild the package

- Clone this repository and its submodules if they are not cloned yet:

```
git clone https://github.com/kamarado/gd32f01x-pack-repo.git
cd gd32f10x-pack-repo
git submodule update --init --recursive
```

- Or, update this repository and submodules if they are already cloned:

```
cd gd32f10x-pack-repo
git pull origin main
```

- Run the build script with Python 3:

```
python build.py
```

[packinstaller]:         http://www2.keil.com/mdk5/packinstaller/
[packs-manager]:         https://gnu-mcu-eclipse.github.io/plugins/packs-manager/
[packs-manager-config]:  https://gnu-mcu-eclipse.github.io/plugins/packs-manager/#configuration
[packs-manager-persp]:   https://gnu-mcu-eclipse.github.io/plugins/packs-manager/#the-packs-perspective
[packs-manager-install]: https://gnu-mcu-eclipse.github.io/plugins/packs-manager/#pack-install
[debug-registers]:       https://gnu-mcu-eclipse.github.io/debug/peripheral-registers/
[pack]:                  https://raw.githubusercontent.com/kamarado/gd32f10x-pack-repo/main/GigaDevice.GD32F10x_DFP.2.0.2.pack
[index.pidx]:            https://raw.githubusercontent.com/kamarado/gd32f10x-pack-repo/main/index.pidx
[index.idx]:             https://raw.githubusercontent.com/kamarado/gd32f10x-pack-repo/main/index.idx
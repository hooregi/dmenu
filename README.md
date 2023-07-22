# Dynamic Menu

`dmenu` is a dynamic menu for X, originally designed for `dwm`. It manages large numbers of user-defined menu items efficiently.

## Upstream

The upstream development for `dmenu` can be found [here](https://git.suckless.org/dmenu).

# Patches

- [alpha](https://tools.suckless.org/dmenu/patches/alpha/)
- [password](https://tools.suckless.org/dmenu/patches/password/)
- [xresources](https://tools.suckless.org/dmenu/patches/xresources/)

# Arch Linux Install

Download the`PKGBUILD` from this repository and run the following command:

```
makepkg -cf
```

This will create a file that ends in `.pkg.tar.zst`. Then run:

```
sudo pacman -U *.pkg.tar.zst
```

# Regular Install

Download the source code from this repository:

```
git clone https://github.com/hooregi/dmenu.git
cd dmenu
sudo make clean install
```

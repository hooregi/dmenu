# Maintainer: Hooregi <hooregi@halo.fm>
pkgname=dmenu-hooregi-git
pkgver=5.0.r580.3a37fcd
pkgrel=1
epoch=
pkgdesc="Hooregi's build of suckless' dynamic menu (dmenu)"
arch=(x86_64)
url="https://gitlab.com/Hooregi/dmenu.git"
license=('MIT')
groups=()
depends=(nerd-fonts-fira-code)
makedepends=(git)
checkdepends=()
optdepends=()
provides=(dmenu)
conflicts=(dmenu)
replaces=()
backup=()
options=()
install=
changelog=
source=("git+$url")
noextract=()
md5sums=('SKIP')
validpgpkeys=()

pkgver() {
	cd "${_pkgname}"
    printf "5.0.r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

build() {
	cd dmenu
    make X11INC=/usr/include/X11 X11LIB=/usr/lib/X11
}

package() {
    cd dmenu
    mkdir -p ${pkgdir}/opt/${pkgname}
    cp -rf * ${pkgdir}/opt/${pkgname}
    make PREFIX=/usr DESTDIR="${pkgdir}" install
    install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
    install -Dm644 README "${pkgdir}/usr/share/doc/${pkgname}/README"
}

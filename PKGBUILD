pkgname=pacwall-git
pkgver=r35.1c28d55
pkgrel=1
pkgdesc="Set the wallpaper to the dependency graph of installed packages"
arch=(any)
url="https://github.com/Kharacternyk/pacwall"
license=('GPL')
depends=(imagemagick graphviz pacman-contrib feh xorg-xdpyinfo)
makedepends=(git)
source=("${pkgname}::git+https://github.com/Kharacternyk/pacwall.git")
md5sums=(SKIP)

pkgver() {
	cd ${pkgname}
	printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
	install -D -m755 "${srcdir}/${pkgname}/pacwall.sh" "$pkgdir/usr/bin/pacwall.sh"
}

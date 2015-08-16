# Maintainer:  Andrzej Giniewicz <gginiu@gmail.com>

pkgname=linuxconsole
pkgver=1.4.6
pkgrel=1
pkgdesc="Set of utilities for joysticks and serial devices"
arch=('i686' 'x86_64')
url="http://sourceforge.net/projects/linuxconsole/"
license=('GPL')
makedepends=('sdl')
provides=('inputattach' 'joystick')
conflicts=('inputattach')
replaces=('joystick')
optdepends=('sdl: for ffmvforce utility')

source=(http://prdownloads.sourceforge.net/linuxconsole/linuxconsoletools-$pkgver.tar.bz2)
md5sums=('9115e08e3a2193b62da46d0e02852787')

build() {
  cd "${srcdir}"/linuxconsoletools-$pkgver
  make
}

package() {
  cd "${srcdir}"/linuxconsoletools-$pkgver
  make PREFIX=/usr DESTDIR="${pkgdir}" install
}


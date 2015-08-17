# Maintainer: t3ddy  <t3ddy1988 "at" gmail {dot} com>
# Contributor: Nick B <Shirakawasuna at gmail _dot_com>

pkgname=plasma-translatoid-plasmoid
pkgver=1.30
pkgrel=2
pkgdesc="A translator plasmoid using google translator."
arch=('i686' 'x86_64')
url="http://www.kde-look.org/content/show.php/translatoid?content=97511"
license=('GPL')
depends=('kdelibs' 'qjson')
makedepends=('cmake' 'automoc4')
source=(http://kde-look.org/CONTENT/content-files/97511-translatoid-${pkgver}.tar.gz)
md5sums=('7f5e2c4d11756da3b0fa9c80076426df')

build() {
  cd $srcdir/translatoid-${pkgver}
  mkdir build && cd build

  cmake -DCMAKE_INSTALL_PREFIX=/usr ../ || return 1
  make || return 1
  make DESTDIR=$pkgdir install || return 1

  rm -r $pkgdir/usr/share/apps/cmake/
}
# $Id: pkgbuild-mode.el,v 1.23 2007/10/20 16:02:14 juergen Exp $
# Maintainer: Alexandre Bique <bique.alexandre@gmail.com>
pkgname=ezxml
pkgver=0.8.6
pkgrel=1
pkgdesc="xml parsing C library"
url="http://ezxml.sourceforge.net"
arch=('i686' 'x86_64')
license=('MIT')
depends=()
makedepends=()
conflicts=()
replaces=()
backup=()
install=
source=(http://prdownloads.sourceforge.net/$pkgname/$pkgname-$pkgver.tar.gz?download)
md5sums=('e22ae17a0bd82dfa2a66f9876f1a8fd7')

build() {
  cd $startdir/src/$pkgname
  gcc -Wall -O2 -fPIC -c -o ezxml.o ezxml.c
  gcc -shared -Wl,-soname,libezxml.so.0 -o libezxml.so
  mkdir -p "$startdir/pkg/usr/lib/"
  mkdir -p "$startdir/pkg/usr/include/"
  install libezxml.so "$startdir/pkg/usr/lib/"
  install ezxml.h "$startdir/pkg/usr/include/"
}

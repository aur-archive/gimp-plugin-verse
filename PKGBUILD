# Maintainer: Lukas Jirkovsky <l.jirkovsky@gmail.com>
pkgname=gimp-plugin-verse
pkgver=r6p1
pkgrel=2
pkgdesc="Views, creates and edits bitmap nodes on a Verse server in realtime"
arch=('i686' 'x86_64')
url="http://users.pandora.be/blendix/verse/"
license=('GPL')
depends=('gimp')
makedepends=('verse-svn')
source=(http://users.pandora.be/blendix/verse/release/verse-gimp-$pkgver.tar.gz)
md5sums=('a73f2d7917bb8653f0a0901a82a33b1d')

build() {
  cd "$srcdir"/verse-gimp-$pkgver

  sed -i 's|\.\./verse|/usr/lib|' Makefile

  make
}

package() {
  cd "$srcdir"/verse-gimp-$pkgver
  install -D -m755 verse_gimp "$pkgdir"/usr/lib/gimp/2.0/plug-ins/verse_gimp
}

# vim:set ts=2 sw=2 et:

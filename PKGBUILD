# $Id: PKGBUILD 142622 2015-10-01 16:10:18Z fyan $
# Maintainer: Felipe Magno de Almeida <felipe.m.almeida__at__gmail.com>

pkgbase=git-buildpackage
pkgname=python2-git-buildpackage
pkgver=20160615
pkgrel=1
pkgdesc="Tizen's git-buildpackage project"
arch=('i686' 'x86_64')
#url="http://pyyaml.org"
license=('GPL')
makedepends=('python2')
#install='python-yaml.install'
source=('git+https://git.tizen.org/cgit/tools/git-buildpackage.git#branch=release-20160615'
        'python2.patch')
sha256sums=('SKIP' '0dd867e79c38ea813db2a263ed51abfc89fdd186259fd7c70a94c39859b4bd99')

build() {
  cd $srcdir/git-buildpackage
  patch -p1 -i $srcdir/python2.patch
}

package() {
  cd $srcdir/git-buildpackage
  python2 setup.py install --prefix=/usr --root=$pkgdir
#  install -m644 -D LICENSE $pkgdir/usr/share/licenses/$pkgname/LICENSE
}

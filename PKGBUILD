# $Id$
# Maintainer: BlackEagle < ike DOT devolder AT gmail DOT com >
pkgname=python2-gflags
pkgver=2.0
pkgrel=3
pkgdesc="Commandline flags module for Python"
arch=('any')
url="http://code.google.com/p/python-gflags"
license=('BSD')
depends=('python2')
makedepends=('python2-distribute')
provides=('python-gflags')
source=("http://${pkgname/python2/python}.googlecode.com/files/${pkgname/python2/python}-${pkgver}.tar.gz")
sha256sums=('311066217acb8cd8519a4c872cb3fe64f02bcf105802bb761ab0de55c2386cd6')

build() {
	cd ${pkgname/python2/python}-${pkgver}
	python2 setup.py build
}

package() {
	cd ${pkgname/python2/python}-${pkgver}
	python2 setup.py install --root=${pkgdir}
	chmod +r ${pkgdir}/* -R
	#install -dm755 ${pkgdir}/usr/share/licenses/${pkgname}
	install -Dm644 AUTHORS ${pkgdir}/usr/share/licenses/${pkgname}/AUTHORS
	install -Dm644 COPYING ${pkgdir}/usr/share/licenses/${pkgname}/COPYING
}

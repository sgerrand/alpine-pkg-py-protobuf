# Contributor: Sasha Gerrand <alpine-pkgs@sgerrand.com>
# Maintainer: Sasha Gerrand <alpine-pkgs@sgerrand.com>
pkgname=py-protobuf
_pkgname=protobuf
pkgver=2.6.1
pkgrel=0
pkgdesc="Protocol Buffers are Google’s data interchange format."
url="https://pypi.python.org/pypi/protobuf"
arch="all"
license="New BSD License"
depends="python"
depends_dev=""
makedepends="python-dev py-setuptools"
install=""
subpackages=""
source="https://pypi.python.org/packages/source/${_pkgname:0:1}/$_pkgname/$_pkgname-$pkgver.tar.gz"

_builddir="$srcdir/$_pkgname-$pkgver"
prepare() {
	local i
	cd "$_builddir"
	for i in $source; do
		case $i in
		*.patch) msg $i; patch -p1 -i "$srcdir"/$i || return 1;;
		esac
	done
}

build() {
	cd "$_builddir"
	python setup.py build || return 1
}

package() {
	cd "$_builddir"
	python setup.py install --prefix=/usr --root="$pkgdir" || return 1
}

md5sums="6bf843912193f70073db7f22e2ea55e2  protobuf-2.6.1.tar.gz"
sha256sums="8faca1fb462ee1be58d00f5efb4ca4f64bde92187fe61fde32615bbee7b3e745  protobuf-2.6.1.tar.gz"
sha512sums="c345b5b2822e7142e27cd6ff4ca4e8cc307acd3673043428073ed260a899c48ac6afa32e290b2d2f0ee54316d1a0f0ec72287604fb372992715a2191fe5623d4  protobuf-2.6.1.tar.gz"

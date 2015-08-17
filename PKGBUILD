# Maintainer: Tom Wambold <tom5760@gmail.com>
pkgname=python-misaka
pkgver=1.0.2
pkgrel=2
pkgdesc='A Python binding for Sundown, a markdown library.'
arch=('i686' 'x86_64')
url='http://misaka.61924.nl/'
license=('MIT')
depends=('python')
options=(!emptydirs)
source=("http://pypi.python.org/packages/source/m/misaka/misaka-$pkgver.tar.gz"
        "LICENSE.txt")
md5sums=('e99649aaa2a1d0dbeec78069fee3551a'
         'efaf082072405a4adb6aa4cb1530a162')

build() {
  cd "$srcdir/misaka-$pkgver"
  python setup.py build
}

package() {
  cd "$srcdir/misaka-$pkgver"
  python setup.py install --root="$pkgdir/" --optimize=1
  install -D -m644 "$srcdir/LICENSE.txt" "$pkgdir/usr/share/licenses/python-misaka/LICENSE"
}

# vim:set ts=2 sw=2 et:

pkgname=ntfpy
pkgver=0.0.12
pkgrel=1
pkgdesc="Python API Wrapper for ntfy.sh"
arch=('any')
url="https://github.com/Nevalicjus/ntfpy"
license=('MIT')
depends=('python')
makedepends=('python-build' 'python-installer')
source=("$url/releases/download/$pkgver/ntfpy-$pkgver.tar.gz")
sha256sums=('SKIP')

build() {
  cd "$srcdir/$pkgname-$pkgver"
  python -m build
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  python -m installer --destdir="$pkgdir/" dist/*.whl

  install -Dm644 LICENSE.md "$pkgdir/usr/share/licenses/$pkgname/LICENSE.md"
}
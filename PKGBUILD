pkgname=odp-git
pkgver=v1.38.0.0
pkgrel=7
pkgdesc="The ODP project is an open-source, cross-platform set of application programming interfaces (APIs) for the networking data plane"
arch=('i686' 'x86_64')
url="https://github.com/OpenDataPlane/odp"
license=('BSD')
depends=('git' 'automake' 'libtool' 'pkgconf' 'libconfig' 'patch' 'autoconf' 'gcc' 'make')
provides=("$pkgname=$pkgver")
conflicts=("$pkgname")
replaces=("$pkgname")
source=("git+https://github.com/OpenDataPlane/odp")
md5sums=('SKIP')

prepare() {
  cd odp
  git checkout "$pkgver"
  ./bootstrap
}

build(){
  cd odp
  ./configure --prefix=/usr --enable-deprecated
  make
}

package() {
  cd odp
  make DESTDIR="$pkgdir/" install
}

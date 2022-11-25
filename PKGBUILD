pkgname=odp-git
pkgver=v1.35.0.0
pkgrel=6
pkgdesc="The ODP project is an open-source, cross-platform set of application programming interfaces (APIs) for the networking data plane"
arch=('i686' 'x86_64')
url="https://github.com/OpenDataPlane/odp"
license=('BSD')
depends=('git' 'automake' 'libtool' 'pkgconf' 'libconfig' 'patch' 'autoconf' 'gcc' 'make')
provides=("$pkgname=$pkgver")
conflicts=("$pkgname")
replaces=("$pkgname")
source=("git+https://github.com/OpenDataPlane/odp"
        'https://raw.githubusercontent.com/testudo-defense/odp-git/master/initialize_odp_u128_t.diff')
md5sums=('SKIP'
         'f2b775671e324dd81b4adc2d21671aee')

prepare() {
  cd odp
  git checkout "$pkgver"
  patch -p0 < ../initialize_odp_u128_t.diff
  ./bootstrap
}

build(){
  cd odp
  ./configure --prefix=/usr
  make
}

package() {
  cd odp
  make DESTDIR="$pkgdir/" install
}

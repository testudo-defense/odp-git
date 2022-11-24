pkgname=odp-git
pkgver=v1.35.0.0
pkgrel=1
pkgdesc="The ODP project is an open-source, cross-platform set of application programming interfaces (APIs) for the networking data plane"
arch=('i686' 'x86_64')
url=""
license=('BSD')
depends=('git' 'automake' 'libtool' 'pkgconf')
provides=("$pkgname=$pkgver")
conflicts=("$pkgname")
replaces=("$pkgname")
source=("git+https://github.com/OpenDataPlane/odp"
        'https://raw.githubusercontent.com/testudo-defense/odp-git/master/initialize_odp_u128_t.diff')
md5sums=('SKIP'
         'f2b775671e324dd81b4adc2d21671aee')

prepare() {
  echo todo finish $PWD
  cd odp
  git checkout "$pkgver"
  patch -p0 < ../initialize_odp_u128_t.diff
}

#build(){
#   patch -p0 < sockets_fix.diff
#   cd "$srcdir/lwipv6-${pkgver}"
#   autoreconf -i
#   if [ "$CARCH" == "x86_64" ]; then
#      ./configure --prefix="${pkgdir}/usr" --disable-static
#   else
#      ./configure --prefix="${pkgdir}/usr" --libdir="${pkgdir}/usr/lib32" --disable-static
#   fi
#   make
#}

#package() {
#   mkdir -p ${pkgdir}/usr/share
#   tar -xf data.tar.gz
#   cp -r usr/share ${pkgdir}/usr/
#   cd "$srcdir/lwipv6-${pkgver}"
#   make install &> /dev/null
#   rm -rf ${pkgdir}/usr/include
#}

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
source=("git+https://github.com/OpenDataPlane/odp#$pkgver"
        '')
md5sums=('SKIP'
         '')

prepare() {
  echo todo finish
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

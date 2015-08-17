# Contributor: Eric Webb <eric AT collectivegenius DOT net> (based on xapian-ruby-bindings by Sean Escriva <sean.escriva@gmail.com>)
pkgname=xapian-ruby1.8-bindings

_xapianver=1.2.19

pkgver=${_xapianver}
pkgrel=1
pkgdesc="Bindings allowing Xapian to be used from Ruby"
arch=('i686' 'x86_64')
license=('GPL')
url="http://www.xapian.org"
depends=("xapian-core=1:${_xapianver}" 'ruby1.8' )
makedepends=("xapian-core=1:${_xapianver}" 'ruby1.8')
source=(http://www.oligarchy.co.uk/xapian/${_xapianver}/xapian-bindings-${_xapianver}.tar.xz)
md5sums=('d473b5493567eb8363d96f1e20721c90')

RUBY=/opt/ruby1.8/bin/ruby

build()
{
  
  cd ${startdir}/src/xapian-bindings-${_xapianver}
  ./configure --prefix=/usr/ --with-ruby RUBY="$RUBY"
  make
  make check

}

package()
{
  cd ${startdir}/src/xapian-bindings-${_xapianver}
  make DESTDIR=${startdir}/pkg/xapian-ruby1.8-bindings install
}

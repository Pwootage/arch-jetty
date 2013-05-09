# Maintainer: Pwootage <pwootage@gmail.com>
pkgname=jetty
pkgver=9.0.2
_builddate=20130417
_jettyver=$pkgver.v$_builddate
pkgrel=1
pkgdesc="Lightweight Servlet v3.0 Container"
arch=('any')
url="https://eclipse.org/jetty/"
license=('Apache' 'EPL')
groups=()
depends=('java-runtime')
makedepends=()
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=('!strip' 'emptydirs')
install=
changelog=
source=(http://download.eclipse.org/jetty/$_jettyver/dist/jetty-distribution-$_jettyver.tar.gz
jetty.service
jetty.sh)
noextract=()
md5sums=('fdd6e8598292bfe1094f21f679eb73b1'
         '9a42bdd56bd11da45e52b314ad76da44'
         '677da3bdd8fbd16d4b8917a9fe0f6f89')

build() {
	echo build
}

package() {
	cd "$srcdir"

	install -dm755 "$pkgdir/etc/jetty"
	install -dm755 "$pkgdir/srv/jetty"
	install -dm755 "$pkgdir/usr/share/jetty"
	
	install -m755 jetty.service "$pkgdir/usr/lib/systemd/system/jetty.service"
	install -m755 jetty.sh "$pkgdir/usr/share/jetty/jetty.sh"
	cp -r "$_jettyver/lib" "$pkgdir/usr/share/jetty/lib"
	cp -r "$_jettyver/resources" "$pkgdir/usr/share/jetty/resources"
	
}

pkgname=corebird
pkgver=1.3
pkgrel=2
pkgdesc="Native Twitter client, built with Gtk3"
arch=('x86_64')
license=('GPL')
url="http://corebird.baedert.org/"
depends=('gtk3' 'glib2' 'rest' 'sqlite' 'libtool' 'libsoup' 'json-glib' 'intltool' 'librsvg' 
           'gst-libav' 'gst-plugins-base' 'libgstgtkskin' 'gst-plugins-good' 'midna-gtk-icon-theme')
makedepends=('vala' 'automake')
source=("https://github.com/baedert/corebird/archive/${pkgver}.tar.gz")
sha1sums=("b2669bc794bfea2b5caa236221d91068406e458e")

build() {
 
 cd ${pkgname}-${pkgver}
   ./autogen.sh \
   --prefix=/usr \
 
  make
}

package() {
  
  cd ${pkgname}-${pkgver}
  
  make DESTDIR="${pkgdir}" install
}


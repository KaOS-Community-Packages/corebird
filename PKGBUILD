pkgname=corebird
pkgver=1.5
pkgrel=1
pkgdesc="Native Twitter client, built with Gtk3"
arch=('x86_64')
license=('GPL')
url="http://corebird.baedert.org/"
depends=('gtk3' 'glib2' 'rest' 'sqlite' 'libtool' 'libsoup' 'json-glib' 'intltool' 'librsvg' 
           'gst-libav' 'gst-plugins-base' 'libgstgtkskin' 'gst-plugins-good' 'breeze-icons')
makedepends=('vala' 'automake')
source=("https://github.com/baedert/corebird/archive/${pkgver}.tar.gz")
sha1sums=("a5319d433079ee3d851c0835433a9f9a081e5f7f")

build() {
 
 cd ${pkgname}-${pkgver}
   ./autogen.sh \
   --prefix=/usr \
   --disable-spellcheck
 
  make
}

package() {
  
  cd ${pkgname}-${pkgver}
  
  make DESTDIR="${pkgdir}" install
}


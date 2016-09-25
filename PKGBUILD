pkgname=corebird
pkgver=1.3.2
pkgrel=1
pkgdesc="Native Twitter client, built with Gtk3"
arch=('x86_64')
license=('GPL')
url="http://corebird.baedert.org/"
depends=('gtk3' 'glib2' 'rest' 'sqlite' 'libtool' 'libsoup' 'json-glib' 'intltool' 'librsvg' 
           'gst-libav' 'gst-plugins-base' 'libgstgtkskin' 'gst-plugins-good' 'breeze-icons')
makedepends=('vala' 'automake')
source=("https://github.com/baedert/corebird/archive/${pkgver}.tar.gz")
sha1sums=("9b0c87443cde439cf5ca5df40671def2ee413a92")

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


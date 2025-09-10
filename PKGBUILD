pkgver=25.10
pkgrel=1
orgpkgname=lubuntu-artwork
upstreampkgver=25.10.2
pkgdesc="LXQt theme: Lubuntu Arc $upstreampkgver"           
arch=('any')                                                      
url="https://github.com/lext-next/lext-lubuntu-artwork"                 
license=('GPL')                                                          
depends=('lxqt-session')                                                   
source=("http://archive.ubuntu.com/ubuntu/pool/universe/l/${orgpkgname}/${orgpkgname}_${upstreampkgver}.tar.xz")                                                            
                                                                                   
sha256sums=('SKIP')  # for testing; replace with real checksum later                 
                                                                                       
package() {
    msg "Current srcdir is: $srcdir"
    msg "Current pkgdir is: $pkgdir"
    set -x
    trap 'set +x' RETURN   # automatically disable tracing on function exit

    install -d "$pkgdir/usr/share/lxqt/themes"
    
    cp -rv "$srcdir"/artwork/src/usr "$pkgdir"
}

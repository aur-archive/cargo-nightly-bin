# Maintainer: Michael Sproul <micsproul@gmail.com>
# Uploader: xico
# Request Changes: https://github.com/michaelsproul/rust-nightly-archlinux
pkgname=cargo-nightly-bin
pkgver=0.0.1_2015.01.04
pkgrel=1
arch=('i686' 'x86_64')
pkgdesc="Cargo downloads your Rust project's dependencies and compiles your project."
url='http://crates.io/'
provides='cargo'
conflicts=('cargo-git')
depends=('rust-nightly-bin')
license=('MIT' 'Apache')
source=("https://static.rust-lang.org/cargo-dist/cargo-nightly-${CARCH}-unknown-linux-gnu.tar.gz")
sha256sums=('SKIP')
options=(staticlibs !strip)

package() {
    cd cargo-nightly-${CARCH}-unknown-linux-gnu
    ./install.sh --prefix=$pkgdir/usr

    # remove manifest file referencing $pkgdir
    rm -f "${pkgdir}/usr/lib/rustlib/manifest-cargo"
}

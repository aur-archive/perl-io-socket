# Maintainer: Jonas Heinrich <onny@project-insanity.org>
# Contributor: Jonas Heinrich <onny@project-insanity.org>

pkgname='perl-io-socket'
pkgver='1.31'
pkgrel='2'
pkgdesc="IO::Socket - Object interface to socket communications for perl"
arch=('any')
license=('PerlArtistic' 'GPL')
options=('!emptydirs')
depends=('perl')
makedepends=()
url="http://search.cpan.org/~gbarr/IO-1.25/lib/IO/Socket.pm"
source=("http://search.cpan.org/CPAN/authors/id/G/GB/GBARR/IO-1.25.tar.gz")
sha512sums=('eb922dc89f3dd5996b3abd5e5ffc17b581f7b40b9128461da5d2f97466606a2775e44cb1a707673a4e9fbcda69318d462e1d6ad44c26c9378c2a5b49fb8c06e2')

build() {
    cd "$srcdir/IO-1.25"
    perl Makefile.PL INSTALLDIRS=vendor
    make
}

package() {
    cd "$srcdir/IO-1.25"
    make DESTDIR=$pkgdir install
}

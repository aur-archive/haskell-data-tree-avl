# Contributor: Arch Haskell Team <arch-haskell@haskell.org>
# Package generated by cabal2arch 0.3.4
pkgname=haskell-data-tree-avl
pkgrel=1
pkgver=0.4
pkgdesc="Balanced binary trees using AVL algorithm."
url="http://hackage.haskell.org/cgi-bin/hackage-scripts/package/Data-Tree-AVL"
license=('custom:BSD3')
arch=('i686' 'x86_64')
makedepends=('ghc' 'haskell-data-cordering')
source=(http://hackage.haskell.org/packages/archive/Data-Tree-AVL/0.4/Data-Tree-AVL-0.4.tar.gz)
install=haskell-data-tree-avl.install
md5sums=('6535f70bad448d6aa56d3bb79095456f')
build() {
    cd $startdir/src/Data-Tree-AVL-0.4
    runhaskell Setup configure --prefix=/usr || return 1
    runhaskell Setup build                   || return 1
    runhaskell Setup register   --gen-script || return 1
    runhaskell Setup unregister --gen-script || return 1
    install -D -m744 register.sh   $startdir/pkg/usr/share/haskell/$pkgname/register.sh
    install    -m744 unregister.sh $startdir/pkg/usr/share/haskell/$pkgname/unregister.sh
    runhaskell Setup copy --destdir=$startdir/pkg || return 1
    install -D -m644 LICENSE $startdir/pkg/usr/share/licenses/$pkgname/LICENSE || return 1
}

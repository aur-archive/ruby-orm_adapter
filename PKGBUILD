# Generated by gem2arch (https://github.com/anatol/gem2arch)
# Maintainer: Anatol Pomozov <anatol.pomozov@gmail.com>

_gemname=orm_adapter
pkgname=ruby-$_gemname
pkgver=0.5.0
pkgrel=1
pkgdesc='orm_adapter provides a single point of entry for using basic features of popular ruby ORMs.  Its target audience is gem authors who want to support many ruby ORMs.'
arch=(any)
url='https://github.com/ianwhite/orm_adapter'
license=(MIT)
depends=(ruby)
options=(!emptydirs)
source=(https://rubygems.org/downloads/$_gemname-$pkgver.gem)
noextract=($_gemname-$pkgver.gem)
sha1sums=('ff5fd8c64daefdaf9a415db82677e0aae843b6b0')

package() {
  local _gemdir="$(ruby -e'puts Gem.default_dir')"
  gem install --ignore-dependencies --no-user-install -i "$pkgdir/$_gemdir" -n "$pkgdir/usr/bin" $_gemname-$pkgver.gem
  rm "$pkgdir/$_gemdir/cache/$_gemname-$pkgver.gem"
  install -D -m644 "$pkgdir/$_gemdir/gems/$_gemname-$pkgver/LICENSE" "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

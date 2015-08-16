# Maintainer: pisuka <tekmon@gmail.com>
pkgname=lein2
pkgver=2.0.0
pkgrel=1
pkgdesc="Leiningen is for automating Clojure projects without setting your hair on fire."
arch=(any)
url="https://github.com/technomancy/leiningen"
license=(EPL)
groups=()
depends=(java-runtime-headless curl)
makedepends=()
optdepends=()
provides=(leiningen2)
conflicts=(leiningen2 leiningen2-git)
replaces=(leiningen2)
backup=()
options=()
install=
source=(https://raw.github.com/technomancy/leiningen/${pkgver}/bin/lein
		https://raw.github.com/technomancy/leiningen/${pkgver}/doc/lein.1
		https://raw.github.com/technomancy/leiningen/${pkgver}/bash_completion.bash
		https://raw.github.com/technomancy/leiningen/${pkgver}/zsh_completion.zsh)
md5sums=('ae61e748a7a9ef2bfca90a80aa0b22a0'
         '2b8815eb866119ff9abafc489f7b849d'
         '1561749a48bc6a3f17627ce6af1d80ba'
         '65a4f962c5483e0b01d1ea3324597228')
package() {
	mkdir -p "${pkgdir}"/usr/bin/ "${pkgdir}"/usr/share/bash-completion/completions/
	install -m 755 -D "${srcdir}"/lein "${pkgdir}"/usr/bin/lein2
	install -D "${srcdir}"/lein.1 "${pkgdir}"/usr/share/man/man1/lein2.1
	install -D "${srcdir}"/bash_completion.bash "${pkgdir}"/usr/share/bash-completion/completions/lein2
	install -D "${srcdir}"/zsh_completion.zsh "${pkgdir}"/usr/share/zsh/site-functions/_lein2
	sed -i 's/lein/lein2/g' "${pkgdir}"/usr/share/man/man1/lein2.1
	sed -i 's/lein/lein2/g' "${pkgdir}"/usr/share/bash-completion/completions/lein2
	sed -i 's/lein/lein2/g' "${pkgdir}"/usr/share/zsh/site-functions/_lein2
}

# vim:set ts=2 sw=2 et:

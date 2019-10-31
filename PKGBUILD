#Maintainer: Heropoo <aiyouyou1000@163.com>

_pkgname='Hack-vim'
pkgname=hack-vim
pkgver=1.0.0
pkgrel=1
pkgdesc='A hack vim config'
arch=(any)
license=(GPL)
depends=('vim')
install="hack-vim.install"
url="https://github.com/heropoo/hack-vim"
#source=("git+https://github.com/heropoo/hack-vim#branch=master")
#sha256sums=("f4e927777406e10ffdfffeab663cd266b3c2967b5c772ab1cf9ea1be852003fa")
	
package() {
	mkdir -p "${pkgdir}/etc/skel/"
	rm -rf "${pkgdir}/etc/skel/.vim"
	rm -f "${pkgdir}/etc/skel/.vimrc"
	cp -rf "${srcdir}/.vim" "${pkgdir}/etc/skel"
	cp -f "${srcdir}/.vimrc" "${pkgdir}/etc/skel"

	mkdir -m 700 -p "${pkgdir}/${HOME}/"
	rm -rf "${pkgdir}/${HOME}/.vim"
	rm -f "${pkgdir}/${HOME}/.vimrc"
	cp -rf "${srcdir}/.vim" "${pkgdir}/${HOME}"
	cp -f "${srcdir}/.vimrc" "${pkgdir}/${HOME}"
}

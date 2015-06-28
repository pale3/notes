# Author: ava1ar <mail(at)ava1ar(dot)info>

pkgname=notes-git
_pkgname=notes
pkgrel=1
pkgdesc="Simple note takling, inspired by pass" 
url="https://github.com/pale3/notes.git" 
license=('GPL')
arch=('any')
depends=('bash' 'tree') 
source=(git+https://github.com/pale3/notes.git) 
sha1sums=('SKIP')

pkgver() {
	cd ${_pkgname}
	echo $(git rev-list --count master).$(git rev-parse --short master)
}

package() { 
	cd ${_pkgname}
	
	mkdir -p "${pkgdir}"/usr/bin
	cp $_pkgname "${pkgdir}"/usr/bin/

	mkdir -p "${pkgdir}"/usr/share/zsh/site-functions/
	cp -R completion/notes.zsh-completion "${pkgdir}"/usr/share/zsh/site-functions/_notes
}

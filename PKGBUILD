pkgname=(
  'pacman-hook-zsh'
  'pacman-hook-zsh-rehash'
  'pacman-hook-remove-locales'
  'pacman-hook-remove-headers'
  'pacman-hook-remove-documentation'
  'pacman-hook-optimize-images'
  )
pkgver=1.7
pkgrel=1
pkgdesc="Pacman hooks metapackage"
arch=('any')
url='https://github.com/grigorii-horos/pacman-hooks'
license=('LGPL')

source=(zsh 90-zsh.hook 90-zsh-rehash.hook remove-locales 10-remove-locales.hook remove-headers 10-remove-headers.hook remove-documentation 10-remove-documentation.hook optimize-images 90-optimize-images.hook)
sha256sums=('SKIP' 'SKIP' 'SKIP' 'SKIP' 'SKIP' 'SKIP' 'SKIP' 'SKIP' 'SKIP' 'SKIP' 'SKIP')

prepare () {
  true
}

build () {
  true
}

package_pacman-hook-zsh() {
  pkgdesc="Pacman hook who will optimize zsh scripts"
  depends=('zsh')
  
  mkdir -p "$pkgdir/usr/share/libalpm/scripts/" "$pkgdir/usr/share/libalpm/hooks/"
  install "$srcdir"/zsh "$pkgdir/usr/share/libalpm/scripts/"
  install "$srcdir"/90-zsh.hook "$pkgdir/usr/share/libalpm/hooks/"
}

package_pacman-hook-zsh-rehash() {
  pkgdesc="Pacman hook who will run zsh rehash"
  depends=('zsh')
  
  mkdir -p "$pkgdir/usr/share/libalpm/hooks/"
  install "$srcdir"/90-zsh-rehash.hook "$pkgdir/usr/share/libalpm/hooks/"
}

package_pacman-hook-remove-locales() {
  pkgdesc="Pacman hook who will remove unuseful locales"
  
  mkdir -p "$pkgdir/usr/share/libalpm/scripts/" "$pkgdir/usr/share/libalpm/hooks/"
  install "$srcdir"/remove-locales "$pkgdir/usr/share/libalpm/scripts/"
  install "$srcdir"/10-remove-locales.hook "$pkgdir/usr/share/libalpm/hooks/"
}

package_pacman-hook-remove-headers() {
  pkgdesc="Pacman hook who will remove headers"
  
  mkdir -p "$pkgdir/usr/share/libalpm/scripts/" "$pkgdir/usr/share/libalpm/hooks/"
  install "$srcdir"/remove-headers "$pkgdir/usr/share/libalpm/scripts/"
  install "$srcdir"/10-remove-headers.hook "$pkgdir/usr/share/libalpm/hooks/"
}

package_pacman-hook-remove-documentation() {
  pkgdesc="Pacman hook who will remove documentation"
  
  mkdir -p "$pkgdir/usr/share/libalpm/scripts/" "$pkgdir/usr/share/libalpm/hooks/"
  install "$srcdir"/remove-documentation "$pkgdir/usr/share/libalpm/scripts/"
  install "$srcdir"/10-remove-documentation.hook "$pkgdir/usr/share/libalpm/hooks/"
}

package_pacman-hook-optimize-images() {
  pkgdesc="Pacman hook who will optimize all images in package"
  depends=('imagemagick' 'optipng' 'jpegoptim' 'pngquant' 'svgo' 'parallel')

  mkdir -p "$pkgdir/usr/share/libalpm/scripts/" "$pkgdir/usr/share/libalpm/hooks/"
  install "$srcdir"/optimize-images "$pkgdir/usr/share/libalpm/scripts/"
  install "$srcdir"/90-optimize-images.hook "$pkgdir/usr/share/libalpm/hooks/"
}

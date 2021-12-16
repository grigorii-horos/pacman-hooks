pkgname=(
  'pacman-hook-zsh'
  'pacman-hook-remove-locales'
  'pacman-hook-remove-headers'
  'pacman-hook-remove-documentation'
  'pacman-hook-optimize-images'
  )
pkgver=1.5
pkgrel=9
pkgdesc="Pacman hooks metapackage"
arch=('any')
url='https://github.com/grigorii-horos/pacman-hooks'
license=('LGPL')

source=()
sha256sums=()

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
  install ../zsh "$pkgdir/usr/share/libalpm/scripts/"
  install ../90-zsh.hook "$pkgdir/usr/share/libalpm/hooks/"
}

package_pacman-hook-remove-locales() {
  pkgdesc="Pacman hook who will remove unuseful locales"
  
  mkdir -p "$pkgdir/usr/share/libalpm/scripts/" "$pkgdir/usr/share/libalpm/hooks/"
  install ../remove-locales "$pkgdir/usr/share/libalpm/scripts/"
  install ../10-remove-locales.hook "$pkgdir/usr/share/libalpm/hooks/"
}

package_pacman-hook-remove-headers() {
  pkgdesc="Pacman hook who will remove headers"
  
  mkdir -p "$pkgdir/usr/share/libalpm/scripts/" "$pkgdir/usr/share/libalpm/hooks/"
  install ../remove-headers "$pkgdir/usr/share/libalpm/scripts/"
  install ../10-remove-headers.hook "$pkgdir/usr/share/libalpm/hooks/"
}

package_pacman-hook-remove-documentation() {
  pkgdesc="Pacman hook who will remove documentation"
  
  mkdir -p "$pkgdir/usr/share/libalpm/scripts/" "$pkgdir/usr/share/libalpm/hooks/"
  install ../remove-documentation "$pkgdir/usr/share/libalpm/scripts/"
  install ../10-remove-documentation.hook "$pkgdir/usr/share/libalpm/hooks/"
}

package_pacman-hook-optimize-images() {
  pkgdesc="Pacman hook who will optimize all images in package"
  depends=('imagemagick' 'optipng' 'jpegoptim' 'svgcleaner')

  mkdir -p "$pkgdir/usr/share/libalpm/scripts/" "$pkgdir/usr/share/libalpm/hooks/"
  install ../optimize-images "$pkgdir/usr/share/libalpm/scripts/"
  install ../90-optimize-images.hook "$pkgdir/usr/share/libalpm/hooks/"
}

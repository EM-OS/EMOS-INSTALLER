
# Maintainer: Eyad Merajuddin(CanadianGamer) <easygamer2019@gmail.com>
pkgname=emos-installer
pkgver=1.0
pkgrel=1
pkgdesc="Graphical installer for EMOS Linux"
arch=('any')
url="https://github.com/EM-OS/EMOS-INSTALLER"
license=('GPL3')
depends=('gum' 'bash' 'arch-install-scripts')
source=("git+$url.git")
sha256sums=('SKIP')

package() {
  # Install main executable
  install -Dm755 "$srcdir/EMOS-INSTALLER/emos-installer.sh" "$pkgdir/usr/bin/emos-installer"

  # Create script directory under /usr/lib instead
  install -dm755 "$pkgdir/usr/lib/emos-installer/scripts"

  # Install all scripts
  for script in "$srcdir/EMOS-INSTALLER/script/"*.sh; do
    install -m755 "$script" "$pkgdir/usr/lib/emos-installer/scripts/"
  done
  # Create symlink for compatibility if needed
  # ln -s /usr/share/emos-installer/scripts "$pkgdir/usr/bin/emos-installer-scripts"
}

# if [[ $EUID -ne 0 ]]; then
#   echo "[INFO] Relaunching as root..."
#   exec sudo "$0" "$@"
# fi

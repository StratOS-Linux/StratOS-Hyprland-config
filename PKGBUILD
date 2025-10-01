# Maintainer: @zstg <zestig@duck.com>
pkgname=stratos-hyprland-config
pkgver=1.0
pkgrel=10
pkgdesc="Hyprland configuration for StratOS"
arch=('any')
license=('GPL3')
depends=(
    'hyprland' 'hyprpaper' 'hypridle' 'hyprlock'
    'waybar' 'stratos-waybar-hyprland-config'
	'vicinae-bin'
    'ghostty'
    'eww' 'stratos-eww-config'
    'stratos-fonts'
    'mako' 'stratos-mako-config'
    'swayosd'
	'thunar'
    'polkit-gnome'
    'wl-clipboard'
    'stratos-wallpapers'
    'conky'
)

optdepends=(
    "bibata-cursor-theme-bin: StratOS' default cursor theme"
    "stratmacs: StratOS' Emacs build"
    'stratmacs-config: Stratmacs configuration'
    'stratos-btop-config: system resource monitor'
    'swaync: recommended notification daemon'
    'rofi: alternate app launcher'
    "zen-browser-bin: StratOS' default browser"
    'nwg-dock-hyprland-bin: Dock for StratOS-Hyprland'
)

source=()
md5sums=()
install=stratos-hyprland-config.install
prepare() {
    cp -r $startdir/.config $srcdir/
    cp -r $startdir/usr $srcdir/
}
package() {
    install -d $pkgdir/etc/skel/.config
    cp -ra $srcdir/.config/hypr/ $pkgdir/etc/skel/.config/

    install -d $pkgdir/usr/local/bin/
    cp -ra $srcdir/usr/local/bin/* $pkgdir/usr/local/bin/
}

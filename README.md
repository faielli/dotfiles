# dotfiles

Configurazioni personali per Arch Linux.

## Contenuto
- **Niri** — compositor Wayland
- **DankMaterialShell** — KDE shell
- **Zsh** — shell config

## Installazione

```bash
git clone --bare https://github.com/faielli/dotfiles.git ~/.dotfiles
alias dotfiles='/usr/bin/git --git-dir=$HOME/.dotfiles/ --work-tree=$HOME'
dotfiles checkout
```

## Pacchetti
```bash
pacman -S --needed - < .pkglist.txt
```

## Icone
MacTahoe icon theme — scaricalo manualmente e copialo in `/usr/share/icons/`:
- Source: https://www.gnome-look.org/p/2299216

```bash
sudo cp -r MacTahoe* /usr/share/icons/
```

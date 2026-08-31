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

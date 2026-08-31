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

## Comandi dotfiles

### Setup su nuova macchina
```bash
git clone --bare https://github.com/faielli/dotfiles.git ~/.dotfiles
alias dotfiles='/usr/bin/git --git-dir=$HOME/.dotfiles/ --work-tree=$HOME'
echo "alias dotfiles='/usr/bin/git --git-dir=\$HOME/.dotfiles/ --work-tree=\$HOME'" >> ~/.zshrc
dotfiles config --local status.showUntrackedFiles no
dotfiles checkout
```

### Aggiungere un nuovo file
```bash
dotfiles add ~/.config/qualcosa
dotfiles commit -m "add: qualcosa"
dotfiles push
```

### Aggiornare file già tracciati
```bash
dotfiles add -u
dotfiles commit -m "update: dotfiles"
dotfiles push
```

### Sync rapido (alias)
```bash
# Aggiungi a .zshrc:
alias dotpush='dotfiles add -u && dotfiles commit -m "update: dotfiles" && dotfiles push'
```

### Vedere cosa è cambiato
```bash
dotfiles status
dotfiles diff
```

### Reinstallare pacchetti
```bash
pacman -S --needed - < .pkglist.txt
yay -S --needed - < .aur-pkglist.txt
```

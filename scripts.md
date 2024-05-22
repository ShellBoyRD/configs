
#### Initial Setup (required for alacritty and fish configs to function properly)
```
sudo pacman -S lsd bat nerd-fonts ripgrep --noconfirm && fc-cache -fv
```

#### Oh-My-Fish (required for fish configs)
```
curl https://raw.githubusercontent.com/oh-my-fish/oh-my-fish/master/bin/install | fish
```

#### NvChad
```
git clone https://github.com/NvChad/starter ~/.config/nvim && nvim
```

#### Move Configs to Proper Locations
```
sudo mv fish/ ~/.config/fish/ 
sudo mv alacritty/ ~/.config/alacritty/
sudo mv paru.conf /etc/paru.conf
sudo mv nanorc /etc/nanorc
```

#### Use cachyos-pacman.conf (If on arch, this will add cachyos repos. Untested and unsupported)
```
mv cachyos-pacman.conf /etc/pacman.conf
```

#### Use Normal pacman.conf (This will remove cachy repos and possibly break cachyos)
```
mv pacman.conf /etc/pacman.conf
```

#### Install paru
```
git clone https://aur.archlinux.org/paru-bin
cd paru-bin
makepkg -si  
cd ..
rm -rf paru/
```

#### Install Tdrop
```
paru -S tdrop --noconfirm
```

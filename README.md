# Arch post install configs

## Install Yay:
```git clone https://aur.archlinux.org/yay.git && cd yay && sudo makepkg -si```

## Pacman config:
Edit this file: /etc/pacman.conf
Unser "Misc", add these two lines:
- Color
- ILoveCandy

## Multiple core compiling:
Edit this file: /etc/makepkg.conf
Change MAKEFLAGS to: 
- MAKEFLAGS="-j$(nproc)"

## Pacman Packages:
```yay -S --noconfirm neofetch htop firefox-developer-edition alacritty git rofi arandr upower feh```



## Rofi:
Clone this https://github.com/adi1090x/rofi

## ZSH, OH-MY-ZSH & P10k:
- ```yay -Sy --noconfirm ttf-meslo-nerd-font-powerlevel10k zsh-theme-powerlevel10k zsh oh-my-zsh-git```
- ```chsh -s /bin/zsh```
- ```echo 'source /usr/share/zsh-theme-powerlevel10k/powerlevel10k.zsh-theme' >>! ~/.zshrc```
- ```p10k configure```

## Vim
- ```yay -S vim vim-airline```
- ```wget https://raw.githubusercontent.com/haraldaarz/Vim-configs/main/vimrc```
- ```mv vimrc .vimrc```

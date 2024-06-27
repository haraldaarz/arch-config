# Arch post install configs

## Install Yay:
- Install git: ```sudo pacman -S git```
- Clone yay: ```git clone https://aur.archlinux.org/yay.git && cd yay ```
- Make yay: ```makepkg -si```

## Pacman config:
Edit this file: /etc/pacman.conf
Unser "Misc", add these two lines:
- Color
- ILoveCandy

## Yay multiple download:
Uncomment ParallelDownloads in /etc/pacman.conf. 

## Multiple core compiling:
Edit this file: /etc/makepkg.conf
Change MAKEFLAGS to: 
- MAKEFLAGS="-j$(nproc)"

## Pacman Packages:
```yay -S --noconfirm neofetch htop alacritty upower feh vi  xorg-xinput pavucontrol bind  vim-nerdtree  tmux python-pip zsh i3status-rust gnu-netcat net-tools fzf fd noto-fonts-emoji openvpn mousepad evince traceroute dosfstools fuse-exfat usbutils ntfs-3g```

## i3 config:
```wget https://raw.githubusercontent.com/haraldaarz/dotfiles/master/i3/config```
```mv config ~/.config/i3/config ```


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

## Touchpad natural scrolling
- Edit the file: /usr/share/X11/xorg.conf.d/40-libinput.conf
- Add ```"Option "NaturalScrolling" "True"``` under the input class that references touchpad.
- Add ```Option "Tapping" "on"``` for touchpad tap clicking.

## i3 Auto window icons
- ```wget https://raw.githubusercontent.com/justbuchanan/i3scripts/master/autoname_workspaces.py -O  ~/.config/i3/scripts/autoname_workspaces.py```
- ```wget https://raw.githubusercontent.com/justbuchanan/i3scripts/master/util.py -O ~/.config/i3/scripts/util.py```
- ```pip install i3ipc fontawesome```
- ```yay -S xorg-xprop```
- ```chmod 755 ~/.config/i3/scripts/autoname_workspaces.py```
- Add the following line to the i3config:
- ```exec_always ~/.config/i3/scripts/autoname_workspaces.py```


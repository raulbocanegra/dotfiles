Clone and run these scripts on a new Linux machine to configure your `bash`/`zshrc` and several development app as follows.

Install zsh and plugins
=======================

## zsh
```sh
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
## powerlevel10k
```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

## Install Nerd fonts
```bash
wget https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Regular.ttf
wget https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Bold.ttf
wget https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Italic.ttf
wget https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Bold%20NF%20Italic.ttf
mv MesloLGS* ~/.local/share/fonts/
fc-cache -f -v
```
[Setup fonts](https://github.com/romkatv/powerlevel10k#manual-font-installation) in your terminal/apps

dotfiles
========
```bash
cd $HOME
git clone git@github.com:raulbocanegra/dotfiles.git
ln -s dotfiles/.config/Code/User/settings.json .config/Code/User/settings.json
ln -s dotfiles/.config/terminator/config .config/terminator/config
ln -sb dotfiles/.zshrc .
ln -sb dotfiles/.vimrc .
ln -sb dotfiles/.profile .
cp dotfiles/aliases.zsh $ZSH/custom/
touch .config/filezilla/sitemanager.xml
```

# ITerm Beautify Documentation

1. Install iTerm2 for mac

```bash
brew cask install iterm2
```

2. Download `oh my zsh`

    after change to zsh , we should **copy bashrc to zshrc**
```bash
# 1. download oh-my-zsh
# 方式一: 使用git 这里下载到~/.oh-my-zsh下
git clone https://github.com/robbyrussell/oh-my-zsh.git ~/.oh-my-zsh
# 方式二: 使用curl
sh -c "$(curl -fsSL https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
# 方式三: 使用wget
sh -c "$(wget https://raw.github.com/robbyrussell/oh-my-zsh/master/tools/install.sh -O -)"

# 2. 备份配置文件(可省略)
cp ~/.zshrc ~/.zshrc.orig

# 3. 创建一个新的配置文件
cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc

# 切换默认shell为zsh
chsh -s /bin/zsh
```

3. Change theme

	we use defalte theme, if you want to change, change`.zshrc`, and install Nerd font from [https://github.com/ryanoasis/nerd-fonts](https://github.com/ryanoasis/nerd-fonts)
```bash
ZSH_THEME="robbyrussell"
```

4. Change color

	use `OneHalfDark.itermcolors` from [https://github.com/mbadolato/iTerm2-Color-Schemes.git](https://github.com/mbadolato/iTerm2-Color-Schemes.git)

	and import in iterm2 `Preference->Profiles->Colors` , we can alse change `Constract` and `Tranparernt`


5. Install Plugins
- zsh-syntax-highlighting
```bash
# 下载命令高亮插件 这里下载到用户名下.zsh文件夹下
sudo git clone https://github.com/zsh-users/zsh-syntax-highlighting ~/.zsh/zsh-syntax-highlighting
# 编辑配置文件，使用插件
vim ~/.zshrc
# add one line
source ~/.zsh/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh
```
- zsh-autosuggestions
```bash
# 下载命令提示插件
sudo git clone https://github.com/zsh-users/zsh-autosuggestions ~/.zsh/zsh-autosuggestions
# 编辑配置文件，使用插件
vim ~/.zshrc
# add one line
source ~/.zsh/zsh-autosuggestions/zsh-autosuggestions.zsh
```



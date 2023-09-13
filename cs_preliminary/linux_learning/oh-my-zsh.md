# archlinux install zsh, use oh-my-zsh to configure zsh and install some plugins for oh-my-zsh

```shell
# 1. 安装zsh
sudo pacman -S zsh zsh-completions
# 2. 使用命令zsh按照引导配置一下，生成.zshrc
zsh
# 3. 确保git curl wget已经安装，如果没有安装，运行如下命令
sudo pacman -S git curl wget
# 4. 使用如下命令安装oh-my-zsh
sh -c "$(wget https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh -O -)"
# 5. 使用如下命令更细oh-my-zsh
omz update  
# 6. 使用如下命令安装以下两款插件，分别是语法高亮和自动建议
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
# 7. 使用如下命令去挑选喜欢的主题并添加三款插件
# ZSH_THEME="rubbyrussell" 配置主题
# plugins=(git archlinux zsh-syntax-highlighting zsh-autosuggestions) 配置插件
vim .zshrc
# 8. 更新配置
source .zshrc
# 9. 将zsh设为默认shell

# 为root设置
sudo chsh -s /bin/zsh root
# 为当前用户设置
chsh -s /bin/zsh
#恢复为默认bash
chsh -s /bin/bash

# 10. 解决windows下vscode远程连接时terminal的一些字符乱码问题
# 下载powerline字体 https://github.com/powerline/fonts
# 进行解压缩
# 找一个字体进行安装
# vscode设置里找到terminal，找到font，更改为你刚才安装的那个字体，terminal>Integrated:Font Family
```
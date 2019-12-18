# msfvenom zsh completion  

![](https://i.imgur.com/DJV1Jie.gif)

## install 

```
# You have to install oh-my-zsh first.

# Download the msfvenom plugin.
git clone https://github.com/Green-m/msfvenom-zsh-completion ~/.oh-my-zsh/custom/plugins/msfvenom/

# Open your ~/.zshrc file and enable msfvenom plugin like below
# plugins=(...  msfvenom)

source ~/.zshrc
```

## bug

If you get stuck into troubles when using it, run `compinit` to reinitialize the zsh completion environment, reference [here](https://github.com/andsens/homeshick/issues/89).


## zsh

zsh 是一个虚拟终端，原先不同的终端有不同的命令，现在通过这个虚拟终端就可以执行所有的命令，如可以执行git命令、subline命令等。
zsh 在 mac 中的安装和使用。
安装
## 安装

    1. sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" "" --unattended

    # 创建配置文件
    2. cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc

    # 设置zsh为默认终端
    3. chsh -s /bin/zsh

## 安装完成后会自带一些主题，也可以去下面的地址下载主题放到 ~/.oh-my-zsh/themes 下

https://github.com/robbyrussell/oh-my-zsh/wiki/themes

修改主题


    1. 打开配置文件：open ~/.zshrc
    2. 修改配置文件：ZSH_THEME=你想要的主题，默认为robbyrussell
    3. 让配置文件生效：source ~/.zshrc
    4. 主题推荐：ys，ys是安装时自带的，无需额外下载

自动补全插件 incr

    1. 下载：http://mimosa-pudica.net/zsh-incremental.html
    2. 进入plugins文件夹：cd ~/.oh-my-zsh/plugins
    3. 创建一个新的文件夹并进入：mkdir incr; cd incr
    4. 创建一个新的文件：touch incr-0.2.zsh
    5. 把下载下来的文件拷贝过来：cp /Users/jasper/Downloads/incr-0.2.zsh incr-0.2.zsh
    6. 赋予该文件最高权限：chmod 777 ~/.oh-my-zsh/plugins/incr/incr-0.2.zsh
    7. 在./zshrc中加入这样一句话：source ~/.oh-my-zsh/plugins/incr/incr-0.2.zsh
    8. 让配置文件生效：source ~/.zshrc
    9. 配置完成，现在已经有自动补全了

路径跳转插件autojump

    其实用到的频率并不高，如果命令行卡的话不建议安装

只要你访问过某路径如/a/b/c/d，那么下次你输入j d就可以快速进入该路径

    1. 找个地方准备下载如Downloads：git clone git://github.com/joelthelion/autojump.git
    2. 进入autojump文件夹：cd autojump
    3. 运行安装文件：./install.py
    4. 根据提示，将下面的命令复制到~/.zshrc中
    [[ -s /Users/jasper/.autojump/etc/profile.d/autojump.sh ]] && source /Users/jasper/.autojump/etc/profile.d/autojump.sh
    5. 更新配置： source ~/.zshrc
    6. 安装完成
    
代码高亮插件zsh-syntax-highlighting

zsh-syntax-highlighting 可以高亮一些常用命令如cd、open等

    1. 下载插件： git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
    2. 在.zshrc的plugins中添加zsh-syntax-highlighting，plugins={... zsh-syntax-highlighting}

不用安装的插件

这些插件只需要在 .zshrc 的 plugins 里面添加即可，如 plugins={git web-search}，添加后需要重启终端

    1. web-search: 可以快速进行搜索，如google test或者baidu test，就会打开浏览器并进行搜索
    2. last-working-dir：打开终端的默认路径为上一次离开时的路径（推荐）
    3. wd: 可以给目录添加索引，进入/a/b/c/d然后执行wd add test，之后无论在哪里执行wd test都会进入到/a/b/c/d


# 程序员的自我修炼: 编程工具篇

编程工具是程序员将创意变为现实的桥梁，包括硬件和软件。选择合适的工具不仅能提升效率，还能显著优化工作体验。本篇将从多个维度探讨工具选择的逻辑与实践，帮助程序员打造更流畅的工作流。内容结构如下：

- 选择计算机
- 选择键盘
- 操作系统
- 编程工具

## 1. 选择计算机

每个程序员的旅程都从一台合适的计算机开始。选择时，需考虑*短板效应*：性能不足的设备会成为效率的瓶颈，尤其是在关键时刻。

### 1.1 购买原则

* **投资视角** ：电脑是生产工具，优质设备是一种高效的时间投资。
* **性能优先** ：稳定流畅的设备能减少非必要问题，专注于编程本身。
* **适度超前配置**：考虑未来几年可能的需求，避免硬件淘汰过快。
* **一步到位** ：选择高性能设备，避免频繁更换带来的额外成本。

### 1.2 笔记本电脑

推荐  **MacBook Pro** 。作为生产力工具，MacBook Pro 的性能、设计和稳定性值得投资 (看到这里, 苹果应该给我打钱)：

- **做工优质** ：苹果的硬件设计和做工在行业内领先，Windows 阵营中仅 Dell XPS 系列可媲美，但其用户体验相对较差。

- **顶级硬件设计**: 触控板、键盘、屏幕、音响等体验优秀。

- **独立于操作系统的硬件选择** ：尽管 macOS 是默认操作系统，后续仍可自行选择 Linux 等替代方案。

### 1.3 台式机与服务器
- 台式机：适合需要高性能、可定制的用户，可自行组装以实现最佳性价比。

- 服务器：推荐使用 Debian 或 Ubuntu, 比较稳定。

## 2. 选择键盘

键盘是程序员的核心工具，影响打字效率与舒适度。

### 2.1. 类型推荐
- 薄膜键盘：预算有限时的基础选择。
- 机械键盘：提供丰富轴体选择（如青轴、红轴、茶轴等），适合追求个性化体验的用户。
- 静电容键盘：推荐 HHKB 系列，以其独特手感深受程序员喜爱。
- 磁轴键盘：如 Wooting，其高精度触发机制适合游戏玩家及特定场景。

### 2.2 客制化键盘
喜欢 DIY 的程序员可以尝试客制化键盘，从轴体到键帽均可定制，享受动手乐趣与高度个性化的体验。

## 3. 操作系统
操作系统是开发环境的基础，其选择取决于需求与使用场景。

#### 3.1 MacOS
推荐使用白苹果:

- **续航优秀**：适合随时随地办公。
- **稳定性高**：避免 Linux 桌面系统可能的兼容性问题。
- **开发友好**：类 Unix 环境，支持 Shell 操作。
- **系统级别的Emacs支持**：对频繁使用 Emacs 快捷键的用户极为友好。

#### 3.2 Linux
适合需要高度自定义与开源工具链的用户：

##### 3.2.1 Linux On Mac
如果是Macbook, 可以体验一下[Asahi Linux](https://asahilinux.or).

另外我还踩过一个坑: MacOS 14.1无法正常安装Asahi Linux, 这也引申出了Linux的另一个问题: 兼容性

但是会有很多兼容性问题: TODO

##### 3.2.2 Linux Virtual Machine
在MacOS和Windows中安装Linux虚拟机是一个不错的方案, 既可以使用Linux里面的软件包, 又可以兼顾原有操作系统的稳定性和生态, 而且一般虚拟机软件(例如parallel desktop) 是会保持快照功能的, 假如虚拟机的重要文件被破坏了, 也可以轻易地恢复

##### 3.2.3 Native Linux

想要体验最原生的Linux系统, 则推荐在PC或者台式机上安装Linux操作系统

###### 3.2.3.1 系统安装工具

推荐使用系统安装工具 [Ventoy](https://github.com/ventoy/Ventoy)

但是这里可能会踩坑: 主板和芯片的版本问题

##### 3.2.3.2 Linux发行版

推荐发行版：
Debian/Ubuntu：稳定优先，适合服务器或主力开发机。
Arch Linux：灵活性强，但硬件驱动需手动配置。如果有时间, 可以体验一下Arch Liux, 系统体验很不错, 但是硬件驱动不是很好, 需要自己费时间去一个个调试

#### 3.3 Windows

适合游戏和特定开发场景（如 C# 开发）。对于其他场景，macOS 和 Linux 更具优势。

## 4. 编程工具

本次节会按照操作系统的维度介绍

### 4.1. MacOS 

#### 4.1.2 Mac系统调优

##### 4.1.2.1 键位映射修改

Caps Lock键换成Ctrl比较好, 因为Unix上很多操作需要经常按Ctrl, 比如Ctrl-C, Ctrl-D
<img width="715" alt="image" src="https://github.com/user-attachments/assets/fbe39666-c410-42d4-9d46-6e4f64fb53f4">

https://github.com/user-attachments/assets/d571fd68-3350-47c5-a039-9457c8fe30eb

##### 4.1.2.2 系统操作调优

MacOS的屏幕面积寸土寸金, 而且平时几乎很少会用dock, 不如直接把dock隐藏掉

```shell
defaults write com.apple.dock autohide-delay -float 1000; killall Dock
```

如果想要暂时显示dock: 可以通过Ctrl-up来显示桌面, 从而显示Dock栏

如果想要恢复dock:

```shell
defaults delete com.apple.dock autohide-delay; killall Dock
```

设置轻触点击

```shell
defaults write com.apple.AppleMultitouchTrackpad Clicking -int 1
defaults -currentHost write NSGlobalDomain com.apple.mouse.tapBehavior -int 1
defaults write NSGlobalDomain com.apple.mouse.tapBehavior -int 1
```

设置三指拖拽

```shell
defaults write com.apple.driver.AppleBluetoothMultitouch.trackpad TrackpadThreeFingerDrag -bool true
defaults write com.apple.AppleMultitouchTrackpad TrackpadThreeFingerDrag -bool true
```

设置全键盘控制

```shell
defaults write NSGlobalDomain AppleKeyboardUIMode -int 3
```

光标移动提速

```shell
defaults write -g ApplePressAndHoldEnabled -bool false
```

取消光标移动提速

```shell
defaults write -g ApplePressAndHoldEnabled -bool true
```

**<u>运行完命中之后, 需要log out之后才能生效</u>**


#####  4.1.2.3 巧用系统级别emacs快捷键

Emacs是神的编辑器，而Vim是编辑器之神。
https://www.cnblogs.com/batcom/archive/2013/04/25/3042426.html

这里就不论战了, 介绍一个兼收并蓄的方法来使用emacs



https://github.com/user-attachments/assets/e3ecbfa8-586b-4777-8263-ddc2d1dee63b


https://github.com/user-attachments/assets/341088fb-9bfb-4e91-bd54-bae4c12b6261



https://github.com/user-attachments/assets/a793404c-79b4-446e-9999-4c8fb83e21f4



但是这个快捷键在Windows和Linux上会有快捷键冲突,  所以也callback了为什么推荐Mac系统


##### 4.1.2.4 在终端需要输入sudo的时候, 使用指纹验证

Enable fingerprint authentication for `sudo`:

```shell
sed "s/^#auth/auth/" /etc/pam.d/sudo_local.template | sudo tee /etc/pam.d/sudo_local
```

<img width="825" alt="image" src="https://github.com/user-attachments/assets/83b41bb4-171c-48c0-8342-4f35344e7e7f">






#### 4.1.3 包管理器

MacOS上最佳的包管理器(其实Linux上也可以使用):

Homebrew

https://brew.sh/

```shell
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

比较geek的做法是直接使用brew来安装所有程序, 而不是手动地一个个地点击下载安装
e.g.

```shell
brew install visual-studio-code
```

#### 4.1.4 Shell设置

##### 4.1.4.1 fish

推荐使用fish
参考教程: https://mmazzarolo.com/blog/2023-11-16-my-fish-shell-setup-on-macos/

##### 4.1.4.5 autojump

`autojump` 可以快速跳转到目标路径, 还有一些其他的操作比如打开目标文件夹

安装autojump

```shell
brew install autojump
```

**Add to `~/.zshrc`:**

```shell
[[ -s $(brew --prefix)/etc/profile.d/autojump.sh ]] && . $(brew --prefix)/etc/profile.d/autojump.sh
```

常用命令:

- Go to directory: `j [directory_name]`
- Open directory: `jo [directory_name]`
- Show database entries: `j -s`


#### 4.1.4 窗口管理
MacOS上比较有名的平铺式窗口管理器yabai: https://github.com/koekeishiya/yabai, 类似Linux中的i3

但是现在已经不使用yabai了, MacOS就像一个精密的仪器, 如果用户按照Apple给的用户手册来操作, 会很舒服, 但是如果像Linux那样去高度定制化这台机器, 最后大概率会失望

#### 4.1.5 编辑器
程序员写代码最重要的一项武器: 编辑器

##### 4.1.5.1 Vim
Vim是一个强大的编辑器, 只要会打字, 就会使用Vim

如果你想要在未来几年从事编程工作, 那么花费几个月的时间学习和熟悉Vim是十分有价值的一笔时间投资

这里推荐一下我当年入门Vim的游戏: https://vim-adventures.com/

TODO来点演示

##### 4.1.5.2 Neovim

Neovim 是Vim 的一个分支，旨在改进和扩展原始的Vim 编辑器

有很多开源项目使用Neovim搭建终端IDE:
- https://www.lunarvim.org/
- https://www.lazyvim.org/

##### 4.1.5.3 VSCode
https://code.visualstudio.com/
程序员应该都听说过

##### 4.1.5.4 Jetbrains
https://www.jetbrains.com/
程序员应该都用过

##### 4.1.5.5 开发工具pattern

vim, vscode, jetbrains 看似是三个东西, 实际上可以是同一个

可以在Jetbrains的IDE中安装Vim插件, 同时改用VSCode的快捷键mapping, 配合Emacs系统级别的快捷键, 就得到了一个缝合怪

##### 4.1.5.6 AI IDE

作为程序员, 可以觉得目前的AI工具比较弱智而不用它, 但是不能不学习它

目前比较有名的AI IDE有
- [cursor](https://www.cursor.com/)
- [windsurf](https://codeium.com/windsurf)

但是目前使用下来总会感觉不够完美, 希望在不久的将来能够用上真正的AI IDE

#### 4.1.6 Mac软件推荐
```shell
brew install keycastr
brew install iterm2
brew install typora
brew install dropbox
brew install hyperswitch
brew install bob
brew install keepassxc
brew install iina
brew install spotify
brew install snipaste
brew install raycast
brew install omnifocus
```

#### 4.1.7 浏览器

还是推荐浏览器的老大哥: Chrome

Arc 浏览器是浏览器中的新锐, 用户体验也是不错, 但是Arc浏览器的跨设备同步功能有点问题, 而且日常使用比较卡, 另外最近还爆出一个安全问题

https://arc.net/blog/CVE-2024-45489-incident-response

##### 4.1.7.1 Chrome插件推荐

[Tampermonkey](https://chromewebstore.google.com/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo)

[Proxy SwitchyOmega](https://chromewebstore.google.com/detail/proxy-switchyomega/padekgcemlokbadohgkifijomclgjgif)

[ModHeader - Modify HTTP headers](https://chromewebstore.google.com/detail/modheader-modify-http-hea/idgpnmonknjnojddfkpgkljpfnnfcklj)


#### 4.1.8 版本管理工具 Git

https://gist.github.com/joshbuchea/6f47e86d2510bce28f8e7f42ae84c716

https://missing.csail.mit.edu/2020/version-control/

常用的git cheat sheet

https://education.github.com/git-cheat-sheet-education.pdf

### 4.2. Linux

大部分的软件和MacOS都差不多, 下面只列举一些Linux上比较独特的

#### 4.2.1 Tmux

经常用做Session的管理, 以及后台进程管理

https://www.redhat.com/en/blog/introduction-tmux-linux

#### 4.2.2 i3

如果用了Linux但是没有[i3](https://i3wm.org), 那么可能错失了Linux一小半的快乐

相比于stack-based window management, 这种tilling window management熟练之后操作会更加高效

这个视频中比较简略地介绍了一下i3: https://www.bilibili.com/video/BV1kg411i7n3/?vd_source=d2c806a9bab81eb0397edea7c98c6980


#### Linux软件推荐

https://github.com/hluk/CopyQ?tab=readme-ov-file

### 4.3. Windows

Windows编程强推WSL2.0, 

## 4.4 云开发

完全使用浏览器进行开发, 也就是所有的开发工作通过浏览器连接远程服务器来完成

### 4.4.1 github codespace

### 4.4.2 compiler explorer
https://godbolt.org/

### 4.4.3 web vscode
https://vscode.dev/

### 4.4.4 colab


### 其他

打字练习网站: https://play.typeracer.com/

# ohmyzsh-gitee

本仓库的目的是使用[Gitee 极速下载/oh-my-zsh](https://gitee.com/mirrors/oh-my-zsh)来下载、安装及升级oh-my-zsh

* 使用Gitee来获取本仓库的install.gitee.sh脚本并安装oh-my-zsh

| Method    | Command                                                                                   |
| :-------- |-------------------------------------------------------------------------------------------|
| **curl**  | `sh -c "$(curl -fsSL https://gitee.com/leok77s/ohmyzsh-gitee/raw/main/install.gitee.sh)"` |
| **wget**  | `sh -c "$(wget -O- https://gitee.com/leok77s/ohmyzsh-gitee/raw/main/install.gitee.sh)"`   |
| **fetch** | `sh -c "$(fetch -o - https://gitee.com/leok77s/ohmyzsh-gitee/raw/main/install.gitee.sh)"` |

原理是将install.sh脚本中的git远程仓库替换为[Gitee 极速下载/oh-my-zsh](https://gitee.com/mirrors/oh-my-zsh)：

```shell
REPO=${REPO:-ohmyzsh/ohmyzsh}
REMOTE=${REMOTE:-https://github.com/${REPO}.git}
```

```shell
# Mirror settings
# https://gitee.com/mirrors/oh-my-zsh
REPO=${REPO:-mirrors/oh-my-zsh}
REMOTE=${REMOTE:-https://gitee.com/${REPO}.git}
```

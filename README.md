# 准备工作
## 踩坑踩了三次，留着给自己以后偷个懒。
下载install.sh，然后cd到对应文件夹，打开terminal

HOMEBREW_CORE_GIT_REMOTE=https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/homebrew-core.git bash install.sh

# 替换上游
## 以下针对 mac OS 系统上的 Homebrew
git -C "$(brew --repo homebrew/core)" remote set-url origin https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/homebrew-core.git

git -C "$(brew --repo homebrew/cask)" remote set-url origin https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/homebrew-cask.git

git -C "$(brew --repo homebrew/cask-fonts)" remote set-url origin https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/homebrew-cask-fonts.git

git -C "$(brew --repo homebrew/cask-drivers)" remote set-url origin https://mirrors.tuna.tsinghua.edu.cn/git/homebrew/homebrew-cask-drivers.git

## 更换后测试工作是否正常
brew update

# 完事儿，收工。

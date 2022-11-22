# Git Bare Repository - A Better Way To Manage Dotfiles
# Distro-tube https://www.youtube.com/watch?v=tBoLDpTWVOM
# Atlassian Tutorial https://www.atlassian.com/git/tutorials/dotfiles

# To configure:

mkdir dotfiles 

git init --bare $HOME/dotfiles 

alias config='/usr/bin/git --git-dir=$HOME/dotfiles/ --work-tree=$HOME' 

config config --local status.showUntrackedFiles no 

 

git remote add dotfiles git@github.com:cyborganizer1/my-dotfiles.git 

config pull --set-upstream git@github.com:cyborganizer1/my-dotfiles.git main 

/* 

config pull --set-upstream git@github.com:cyborganizer1/my-dotfiles.git main --allow-unrelated-histories 

config config pull.rebase false 

*/ 

config pull --set-upstream git@github.com:cyborganizer1/my-dotfiles.git main 

 

config add .zshrc 

config commit -m "Add zshrc" 

config push 


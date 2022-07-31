# Git Bare Repository - A Better Way To Manage Dotfiles
# Distro-tube https://www.youtube.com/watch?v=tBoLDpTWVOM

# To configure:

git init --bare $HOME/dotfiles # init bare repo in dotfiles path

alias config='/usr/bin/git --git-dir=$HOME/dotfiles/ --work-tree=$HOME' # set alias to config 

config config --local status.showUntrackedFiles no

git remote add origin git@gitlab.com:linux-files1/dotfiles.git # set remote to existing repo from gitlab

config push git@gitlab.com:linux-files1/dotfiles.git # push to existing repo from gitlab

config push --set-upstream origin main # set upstream

config push

# Once this is done, you will only need to commit changes


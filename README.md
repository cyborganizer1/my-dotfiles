# Git Bare Repository - A Better Way To Manage Dotfiles
# Distro-tube https://www.youtube.com/watch?v=tBoLDpTWVOM

git init --bare $HOME/dotfiles

config config --local status.showUntrackedFiles no

git remote add origin git@gitlab.com:linux-files1/dotfiles.git

config push git@gitlab.com:linux-files1/dotfiles.git

config push --set-upstream origin main

config push

# Once this is done, you will only need to commit changes


## notes
  - don't install 2 programs at the same time
  - search if a package is available in the software center first before downloading a deb file

## install git
  - sudo apt-get install git-core

## install terminator
  - sudo apt-get install terminator

##install vim
  - sudo apt-get intsll vim

## install rvm
```sh
  \curl -sSL https://get.rvm.io | bash -s -- --ignore-dotfiles
  echo "source $HOME/.rvm/scripts/rvm" >> ~/.bash_profile
  source /home/jim/.rvm/scripts/rvm
  rvm install 2.1.1
```

## load dotfiles
```sh
  git clone git:github.com/jvnill/dotfiles.git ~/dotfiles
  ln -s ~/dotfiles/vim/vimrc ~/.vimrc
  ln -s ~/dotfiles/bash/bashrc ~/.bashrc
  ln -s ~/dotfiles/bash/terminator_config ~/.config/terminator/config
  ln -s ~/dotfiles/bash/git_bash_prompt ~/.git_bash_prompt
  ln -s ~/dotfiles/git/gitignore ~/.gitignore
  ln -s ~/dotfiles/git/gitconfig ~/.gitconfig
```

## packages to install
```sh
  # for nokogiri
  sudo apt-get install libxml2 libxml2-dev libxslt1-dev

  # for mysql
  sudo apt-get install mysql-server mysql-client libmysqlclient-dev

  # for postgresql
  sudo apt-get install libpq-dev postgresql-client postgresql postgresql-contrib

  # for a working javascript runtime
  sudo apt-get install nodejs

  # heroku toolbelt
  wget -qO- https://toolbelt.heroku.com/install-ubuntu.sh | sh
```

## CREATING a postgresql user
```sh
  sudo -u postgres createuser --superuser $USER
  sudo -u postgres psql
    >> \password jim
```

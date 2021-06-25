# How To (this should help building all of the projects excluding the Website)

## Install Homebrew

`/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

to verify run `brew doctor`

If you get something like `Your system is ready to brew` you are good to go.

## Install Git

`brew update && brew install git`

and to verify if it's ok run
`git --version`

## Install RVM with latest Ruby and Rails

`curl -L https://get.rvm.io | bash -s stable --auto-dotfiles --autolibs=enable --rails`

and then run

`source /Users/__YOUR_USERNAME__/.rvm/scripts/rvm`

which will allow you to use `rvm` in current terminal window.

When that's done you can install whatever version of Ruby you need by e.g.
`rvm install "ruby-2.4.1"` (this will install version 2.4.1 which we are using currently in consent form builder project - as of 2018.07.31)

## Install Bundler

`gem install bundler`

## Install Hivemind

`brew install hivemind`

## Install NVM

This is a script for using different versions of Node and NPM
To install run:

`brew update && brew install nvm`

then create .nvm directory by:

`mkdir ~/.nvm`

update you `.bash_profile` by running e.g.

`vim .bash_profile`

and adding

`export NVM_DIR="$HOME/.nvm" . "/usr/local/opt/nvm/nvm.sh"`

to your `.bash_profile`

(in Vim press the `A` key, paste mentioned lines, press ESC key, shift+colon, type `wq`), press enter)

then run:

`source ~/.bash_profile`

Now you can install any Node version you need. We are using latest LTS version. In order to install it run:

`nvm install --lts=carbon` or `nvm install 8.11.3` (which is current latest LTS version as of 2018.07.31)

## Install PostreSQL

`brew install postgresql`

You will probably need this as a service running in the background so run:

`brew services start postgresql`

## Install Yarn (with brew and nvm present)

`brew install yarn --without-node`

## Setup Git

`git config --global user.name "Tony Stark"`

`git config --global user.email tony@starkenterprises.com`

## Setup git 2FA

generate new key

`ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`

run agent

`eval "$(ssh-agent -s)"`

on macOS 10.12.2 + run

`vim ~/.ssh/config`

and paste in:

`Host * AddKeysToAgent yes UseKeychain yes IdentityFile ~/.ssh/id_rsa`

add private ssh to ssh-agent

`ssh-add -K ~/.ssh/id_rsa`

add ssh key to github

`pbcopy < ~/.ssh/id_rsa.pub`

## If you have issues building your test database (consent_test)

`CREATE USER consent; CREATE USER consent_test; CREATE DATABASE consent OWNER consent; CREATE DATABASE consent_test OWNER consent_test;`

## Extras (you don't need it but you can have it)

`gem install ruby-debug-ide`

`gem install debase`

`brew install bash-completion`

then add

if [ -f `brew --prefix`/etc/bash_completion.d/git-completion.bash ]; then
. `brew --prefix`/etc/bash_completion.d/git-completion.bash
fi

in .bash_profile

`brew install bash-git-prompt`

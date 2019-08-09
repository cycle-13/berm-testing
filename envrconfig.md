# Development Environment Config

Code Editor
    * SublimeText https://www.sublimetext.com/3
    * Atom https://atom.io
    * VS Code https://code.visualstudio.com
    * VS Codium https://github.com/VSCodium/vscodium/releases

Terminal Emulators and Command-line Interpreters
    * https://gnometerminator.blogspot.com/p/introduction.html
    * https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html
    * https://github.com/Swordfish90/cool-retro-term
    * https://conemu.github.io
    * https://cmder.net

### Debian Distro
Sublime Text
* `$ wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -`
* `$ sudo apt-get install apt-transport-https`
* `$ echo "deb https://download.sublimetext.com/ apt/stable/" | sudo tee /etc/apt/sources.list.d/sublime-text.list`

Git
* `$ sudo apt-get install build-essential`
* `$ sudo apt-get install g++'`
* `$ sudo apt-get install -y libssl-dev libreadline-dev zlib1g-dev`
* `$ sudo apt-get install libsqlite3-dev`
* `$ sudo apt-get install git`

Rbenv
* $ git clone https://github.com/rbenv/rbenv.git ~/.rbenv
* $ mkdir -p "$(rbenv root)"/plugins
* $ git clone https://github.com/rbenv/ruby-build.git "$(rbenv root)"/plugins/ruby-build
* $ echo 'export PATH="$HOME/.rbenv/bin:$PATH"'
* $ echo 'eval "$(rbenv init -)"'
* $ curl -fsSL https://github.com/rbenv/rbenv-installer/raw/master/bin/rbenv-doctor | bash

Ruby < 2.4 is not compatible with openssl 1.1
Need to install libssl1.0-dev
`curl https://cli-assets.heroku.com/install.sh | sh`

$ sudo apt-get install freetds-dev
$ gem install tiny-tds
$ gem install activerecord-sqlserver-adapter

### Windows
* System Properties -> Advanced System Settings -> Advanced -> Environment Variables
    * Shortcut is to open command line and type `sysdm.cpl`
    * Create a new system variable called SUBLIME that will point to the folder of your Sublime installation
        * To add the System Variable to PATH, Add the following to the end of your PATH variable: ;%SUBLIME%
        * New commands
            * `subl.exe` and `subl` both launch app
            * `subl .` opens current folder within app

### Checks
* bash --version
* git --version
* python --version
* ruby -v
* rails -v
* rbenv -v
* heroku -v
* npm -v
* node -v

### Gitignore
Bash
`git config --global core.excludesfile ~/.gitignore`

cmd.exe
`git config --global core.excludesfile %USERPROFILE%\.gitignore`

Results in an entry in .gitconfig:
`[core]`
`excludesfile = C:/Users/username/.gitignore_global`

.gitignore_global file contents

    #compiled source
    *.com
    *.class
    *.dll
    *.exe
    *.o
    *.so
     
    # Packages
    *.7z
    *.dmg
    *.gz
    *.iso
    *.jar
    *.rar
    *.tar
    *.zip
     
    # Logs and databases
    *.log
    log/*
    *.sql
    *.sqlite
    *.sqlite3
    *.sqlite3-journal
     
    # OS generated files
    .DS_Store
    .DS_Store?
    ._*
    *.app
    .Spotlight-V100
    .Trashes
    ehthumbs.db
    Thumbs.db
    *.excludes
    *.json
     
    # codekit
    .sass-cache/
    .codekit-config.json
    config.codekit
    
    # Node
    npm-debug.log

    # C++ objects and libs
    *.slo
    *.lo
    *.o
    *.a
    *.la
    *.lai
    *.so
    *.dll
    *.dylib

    # Qt-es
    /.qmake.cache
    /.qmake.stash
    *.pro.user
    *.pro.user.*
    *.moc
    moc_*.cpp
    qrc_*.cpp
    ui_*.h
    Makefile*
    *-build-*
    
    # WebStorm
    .idea/
    
    # vi
    *~

    # Others
    *.xcf
    *.autosave

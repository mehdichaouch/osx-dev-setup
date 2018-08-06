# Developers, all you need to setup your Mac OS X

[![Gitter chat](https://badges.gitter.im/mehdichaouch/1e2740e07f81820ee7df2c47cc193aac.svg)](https://gitter.im/mehdichaouch/1e2740e07f81820ee7df2c47cc193aac)
[![Analytics](https://ga-beacon.appspot.com/UA-77192040-1/mehdichaouch/1e2740e07f81820ee7df2c47cc193aac?pixel)](https://github.com/mehdichaouch/1e2740e07f81820ee7df2c47cc193aac)


After many years on a Dell XPS m1330, I decided to buy my first Mac and write this Mac OS X setup to help others dev like some other devs <sup>[1](#osx-dev-setup-footnote-1)</sup> <sup>[2](#osx-dev-setup-footnote-2)</sup> =)

The document lists all the app I'm using or found interesting, and it assumes you are new to Mac.
The environment will be not set up for a specific language and steps below were tested on OS X El Captain.

As you read and followed those steps, feel free to send me any feedback or comments you may have [on Twitter](https://twitter.com/mehdichch)!


## Table of Contents

| 1                                            | 2                                           | 3                                           | 4                                         | 5                                   |
| -------------------------------------------  | ------------------------------------------- | ------------------------------------------- | ----------------------------------------- | ----------------------------------- |
| [System update](#system-update)              | [System preferences](#system-preferences)   | [Monolingual](#monolingual)                 | [Command Line Tools](#command-line-tools) | [Google Chrome](#google-chrome)     |
| [Oh My Zsh](#oh-my-zsh)                      | [Homebrew](#homebrew)                       | [iTerm2](#iterm2)                           | [GIT](#git)                               | [SourceTree](#sourcetree)           |
| [Sublime Text 3](#sublime-text-3)            | [Google Drive](#google-drive)               | [KeePassX](#keepassx)                       | [f.lux](#flux)                            | [Heroku Toolbelt](#heroku-toolbelt) |
| [Evernote](#evernote)                        | [Spectacle](#spectacle)                     | [Dash](#dash)                               | [XtraFinder](#xtrafinder)                 | [Alfred 2](#alfred-2)               |
| [VLC](#vlc)                                  | [The Unarchiver](#the-unarchiver)           | [Cyberduck](#cyberduck)                     | [Sequel Pro](#sequel-pro)                 | [Caffeine](#caffeine)               |
| [JDK](jdk)                                   | [ClipMenu](#clipmenu)                       | [Dropbox](#dropbox)                         | [Atom](#atom)                             | [N1](#n1)                           |
| [Virtualbox + Vagrant](#virtualbox--vagrant) | [PhpStorm](#phpstorm)                       | [SSHFS](#sshfs)                             | [htop](#htop)                             | [ImageMagick](#imagemagick)         |
| [Certbot](#certbot)                          | [Composer](#composer)                       | [Composer-completion](#composer-completion) | [Php-code-sniffer](#php-code-sniffer)     | [Phpmd](#phpmd)                     |
| [PHP-CS-Fixer](#php-cs-fixer)                | [Mou](#mou)                                 | [Mysql](#mysql)                             | [FileZilla](#filezilla)                   | [Istat-menus](#istat-menus)         |
| [Git-Flow](#git-flow)                        |


## System update

First thing you need to do, on any OS actually, is update the system! For that: _Apple Icon > Software Update..._

**[⬆ back to top](#table-of-contents)**


## System preferences

- Cleaning the dock
- [Show File Name Extensions in Mac OS X](http://osxdaily.com/2012/01/13/show-filename-extensions-in-mac-os-x/)
- [Show Hidden Files in Mac OS X](http://osxdaily.com/2009/02/25/show-hidden-files-in-os-x/)
- Mac keyboard shortcuts](http://support.apple.com/kb/ht1343)

**[⬆ back to top](#table-of-contents)**


## Command Line Tools

Since OS X 10.9 Mavericks, it's possible to install the _Xcode Command Line Tools_ directly from the command line with :
```bash
$ xcode-select --install
```
No need to go through the download page and the survey as describe [here](https://github.com/nicolashery/mac-dev-setup#user-content-install).

**[⬆ back to top](#table-of-contents)**


## Homebrew

[Homebrew](http://brew.sh/) is the missing package manager for OS X. It's some kind of ports for Mac. As a developer, you should install it by flowing : [http://brew.sh/](http://brew.sh/)

Open a new terminal tab with Cmd+T (you should also close the old one), then run the following command to make sure everything works:
```bash
$ brew doctor
```
**[⬆ back to top](#table-of-contents)**


## Oh My Zsh

[Oh My Zsh](https://github.com/robbyrussell/oh-my-zsh)
ZSH is a pretty powerful shell for *nix systems. As a developer, it just changed my life. I don't even know how I lived before using it. No, really, install it NOW: [https://github.com/robbyrussell/oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh)

**[⬆ back to top](#table-of-contents)**


## Monolingual

[Monolingual](https://ingmarstein.github.io/Monolingual/) is a program for removing unnecessary language resources from OS X, in order to reclaim several hundred megabytes of disk space. I save ~780 Mo B)
```bash
$ brew cask install monolingual
```
**[⬆ back to top](#table-of-contents)**


## Google Chrome

[Google Chrome](https://www.google.com/chrome/), no need to present it.
```bash
$ brew cask install google-chrome
```
* synch your account
* install some extension
  * [AdBlock](https://www.getadblock.com/), with my configuration
```
@@||www.advocodo.com/$document
@@||www.advocodo.fr/$document
@@||jiraicoderchezvous.com/$document
@@||jiraicoderchezvous.fr/$document
@@|http://korben.info/|$document
@@|http://mafreebox.freebox.fr/|$document
@@|http://www.6play.fr/m6/direct|$document
@@||www.poulpeo.com/$document
@@|https://magento.com/security/sign-up|$document
@@|https://stickers.notifuse.com/|$document
@@||www.wired.com/$document
@@||public-api.wordpress.com/$document
@@||fr.gravatar.com/$document
@@||mixmax.com/$document
www.blogger.com##SPAN[class="gb_yb"]
bonpatron.com##DIV[id="top"]
bonpatron.com##TD[id="topbanner"]
bonpatron.com##DIV[class="guidetoc"]
www.scribens.fr##DIV[id="Titre"][class="row main-Title"]
www.scribens.fr##HEADER[class="menu-header navbar-fixed-top"]
www.tousaurestaurant.com##DIV[class="logo_wrapper"]
www.silksoftware.com##HEADER[id="masthead"][class="site-header"]
www.coinwarz.com##IFRAME[src="https://refbanners.website/I?tag=d_29508m_1855c_&site=29508&ad=1855"]
www.coinwarz.com##IFRAME[id="takeoverRight"]
www.coinwarz.com##IFRAME[id="takeoverLeft"]
```
  * [uMatrix](https://chrome.google.com/webstore/detail/umatrix/ogfcmafjalglgifnmanfmnieipoejdcf)
  * [Wappalyzer](https://chrome.google.com/webstore/detail/wappalyzer/gppongmhjkpfnbhagpmjfkannfbllamg)
  * [The Great Suspender](https://chrome.google.com/webstore/detail/the-great-suspender/klbibkeccnjlkjkiokjodocebajanakg)
  * [Postman](https://chrome.google.com/webstore/detail/postman/fhbjgbiflinjbdggehcddcbncdddomop)
  * [JSON Formatter](https://chrome.google.com/webstore/detail/json-formatter/bcjindcccaagfpapjjmafapmmgkkhgoa)
  * [Giphy for Chrome](https://chrome.google.com/webstore/detail/giphy-for-chrome/jlleokkdhkflpmghiioglgmnminbekdi)
  * [Ghostery](https://chrome.google.com/webstore/detail/ghostery/mlomiejdfkolichcflejclcbmpeaniij)
  * [Cookies](https://chrome.google.com/webstore/detail/cookies/iphcomljdfghbkdcfndaijbokpgddeno)
  * [Full Page Screen Capture](https://chrome.google.com/webstore/detail/full-page-screen-capture/fdpohaocaechififmbbbbbknoalclacl)

And all of yours ;)

**[⬆ back to top](#table-of-contents)**


## iTerm2

[iTerm2](http://iterm2.com/) is a replacement for Terminal and the successor to iTerm
```bash
$ brew cask install iterm2
```
For the config, follow [https://github.com/nicolashery/mac-dev-setup#iterm2](https://github.com/nicolashery/mac-dev-setup#iterm2)

[http://ethanschoonover.com/solarized/files/solarized.zip](http://ethanschoonover.com/solarized/files/solarized.zip)

**[⬆ back to top](#table-of-contents)**


## GIT

[GIT](https://git-scm.com/) doesn't need any presentation.
```bash
$ brew install git
```

[https://github.com/nicolashery/mac-dev-setup#git](https://github.com/nicolashery/mac-dev-setup#git)
```bash
$ sudo mv /usr/bin/git /usr/bin/git-apple
```
Replace the local GIT with the one installed by brew <sup>[2](#osx-dev-setup-footnote-2)</sup>.

**[⬆ back to top](#table-of-contents)**

## ssh-copy-id

[ssh-copy-id](https://github.com/Homebrew/homebrew-core/blob/master/Formula/ssh-copy-id.rb) ...
```bash
$ brew install ssh-copy-id
```
**[⬆ back to top](#table-of-contents)**


## SourceTree

[SourceTree](https://www.sourcetreeapp.com/) is a free Mercurial and Git Client that provides a graphical interface for your Hg and Git repositories.
```bash
$ brew cask install sourcetree
```
**[⬆ back to top](#table-of-contents)**


## Sublime Text 3

[Sublime Text 3](http://www.sublimetext.com/3) is a sophisticated text editor for code, markup and prose.
```bash
$ brew cask install sublime-text3
```

Conf: [https://github.com/nicolashery/mac-dev-setup#sublime-text](https://github.com/nicolashery/mac-dev-setup#sublime-text)
```bash
$ cd ~/Library/Application\ Support/Sublime\ Text\ 3/Packages/
```
**[⬆ back to top](#table-of-contents)**


## Google Drive

[Google Drive](https://www.google.com/drive/) is a free way to keep your files backed up and easy to reach from any phone, tablet, or computer. Start with 15GB of Google storage.
```bash
$ brew cask info google-drive
```
**[⬆ back to top](#table-of-contents)**


## KeePassX

[KeePassX](https://www.keepassx.org/) is a free, open source, and light-weight password management utility.
```bash
$ brew cask install keepassx
```
**[⬆ back to top](#table-of-contents)**


## f.lux

[f.lux](https://justgetflux.com/) is free software that warms up your computer display at night, to match your indoor lighting.
```bash
$ brew cask install flux
```
**[⬆ back to top](#table-of-contents)**


## Heroku Toolbelt

[Heroku Toolbelt](https://github.com/nicolashery/mac-dev-setup#heroku)
```bash
$ brew install heroku-toolbelt
```
**[⬆ back to top](#table-of-contents)**


## Evernote

[Evernote](https://evernote.com/) is designed for note taking, organizing, and archiving. The app allows users to create a "note" which can be a piece of formatted text, a full webpage or webpage excerpt, a photograph, a voice memo, or a handwritten "ink" note. Notes can also have file attachments. Notebooks can be added to a stack while notes can be sorted into a notebook, tagged, annotated, edited, given comments, searched, and exported as part of a notebook.
```bash
$ brew cask install evernote
```
**[⬆ back to top](#table-of-contents)**


## Spectacle

[Spectacle](http://spectacleapp.com) let you move and resize windows with ease. Window control with simple, customizable keyboard shortcuts. It works only with mouse.
```bash
$ brew cask install spectacle
```
**[⬆ back to top](#table-of-contents)**


## Dash

[Dash](https://kapeli.com/dash) provides fast, offline access to documentation of pretty much everything: programming languages, frameworks, and libraries.
```bash
$ brew cask install dash
```
**[⬆ back to top](#table-of-contents)**


## XtraFinder

[XtraFinder](http://www.trankynam.com/xtrafinder/) adds lots of enhancements to Finder, such as a context menu with _New Text File_, _New Terminal Here_, _Copy Path_, and others.
```bash
$ brew cask install xtrafinder
```
**[⬆ back to top](#table-of-contents)**


## Alfred 2

[Alfred 2](https://www.alfredapp.com/) is a productivity application for Mac OS X, which boosts your efficiency with hotkeys and keywords. Search your Mac and the web, and control your Mac using custom actions with the Powerpack.
```bash
$ brew cask install alfred
```
**[⬆ back to top](#table-of-contents)**


## VLC

[VLC](https://www.videolan.org/vlc/) is a free and open source cross-platform multimedia player and framework that plays most multimedia files, and various streaming protocols.
```bash
$ brew cask install vlc
```
**[⬆ back to top](#table-of-contents)**


## The Unarchiver

[The Unarchiver](https://unarchiver.c3.cx/unarchiver/) is a small and easy to use program that can unarchive many different kinds of archive files. It will open common formats such as Zip, RAR...
```bash
$ brew cask install the-unarchiver
```
**[⬆ back to top](#table-of-contents)**


## Cyberduck

[Cyberduck](https://cyberduck.io/) Libre FTP, SFTP, WebDAV, S3, Backblaze B2, Azure & OpenStack Swift browser.
```bash
$ brew cask install cyberduck
```
**[⬆ back to top](#table-of-contents)**


## Sequel Pro

[Sequel Pro](http://www.sequelpro.com/) is a fast, easy-to-use database management application for working with MySQL/MariaDB databases.
```bash
$ brew cask install sequel-pro
```
**[⬆ back to top](#table-of-contents)**


## Caffeine

[Caffeine](http://lightheadsw.com/caffeine/) is a tiny program that prevent your Mac from automatically going to sleep, dimming the screen or starting screen savers.
```bash
$ brew cask install caffeine
```
**[⬆ back to top](#table-of-contents)**


## JDK

[Java Standard Edition Development Kit](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html) is required to run Java applications.
```bash
$ brew cask install java
```
**[⬆ back to top](#table-of-contents)**


## ClipMenu

[ClipMenu](http://www.clipmenu.com/) can manage clipboard history. You can record 8 clipboard types, from plain text to image.
```bash
$ brew cask install clipmenu
```
**[⬆ back to top](#table-of-contents)**


## Dropbox

[Dropbox](http://www.dropbox.com/) store, sync, and share files (documents, photos, videos, etc.) securely. Ideal for quick devs.
```bash
$ brew cask install dropbox
```
**[⬆ back to top](#table-of-contents)**


## Atom

[Atom](https://atom.io/) is a hackable text editor for the 21st century, built on Electron.
```bash
$ brew cask install atom
```
You will find all my favorite packages on my profile [here](https://atom.io/users/mehdichaouch/stars).
Quickest way to install all my stars package run this buddy:
```bash
$ apm install minimap atom-beautify linter file-icons pigments emmet git-plus highlight-line atom-autocomplete-php javascript-snippets open-recent livereload aligner-php symfony-snippets atom-symfony2 autoclose syfi
```
**[⬆ back to top](#table-of-contents)**


## N1

[N1](https://nylas.com/N1/) is an extensible desktop mail app built on the modern web.
```bash
$ brew cask install nylas-n1
```
**[⬆ back to top](#table-of-contents)**


## Virtualbox + Vagrant

[virtualbox](https://www.virtualbox.org/) is a general-purpose full virtualizer for x86 hardware, targeted at server, desktop and embedded use.

[virtualbox-extension-pack](xxxxxxxx) Add new capabilities to VirtualBox with this extension pack.

[vagrant](https://www.vagrantup.com/) enables users to create and configure lightweight, reproducible, and portable development environments.
```bash
brew cask install virtualbox virtualbox-extension-pack vagrant
```
after install run
```bash
vagrant plugin install vagrant-bindfs
```
**[⬆ back to top](#table-of-contents)**


## PhpStorm

[PhpStorm](https://www.jetbrains.com/phpstorm/) is perfect for working with Symfony, Drupal, WordPress, Zend Framework, Laravel, Magento, Joomla!, CakePHP, Yii, and other frameworks..
```bash
brew cask install phpstorm
```
**[⬆ back to top](#table-of-contents)**


## SSHFS

[SSHFS](https://osxfuse.github.io/) is File system client based on SSH File Transfer Protocol.
```bash
brew cask install sshfs
```
**[⬆ back to top](#table-of-contents)**


## htop

[htop](https://github.com/max-horvath/htop-osx), improved top (interactive process viewer) for macOS.
```bash
brew install htop-osx
```
**[⬆ back to top](#table-of-contents)**


## ImageMagick

[ImageMagick](https://www.imagemagick.org/) is a tools and libraries to manipulate images in many formats.
```bash
brew install imagemagick
```
**[⬆ back to top](#table-of-contents)**


## Certbot

[Certbot](https://certbot.eff.org/) is a tool to obtain certs from Let's Encrypt and autoenable HTTPS.
```bash
brew install certbot
```
**[⬆ back to top](#table-of-contents)**


## Composer

[Composer](https://getcomposer.org) is a Dependency Manager for PHP.
```bash
brew install homebrew/php/composer
```
**[⬆ back to top](#table-of-contents)**


## Composer-completion

[Composer-completion](https://gist.github.com/tonglil/753d59d6d649f85600fe) is a bash completion for Composer.
```bash
brew install homebrew/completions/composer-completion
```
**[⬆ back to top](#table-of-contents)**


## Php-code-sniffer

[Php-code-sniffer](https://pear.php.net/package/PHP_CodeSniffer) check coding standards in PHP, JavaScript and CSS.
```bash
brew install homebrew/php/php-code-sniffer
```
**[⬆ back to top](#table-of-contents)**


## Phpmd

[Phpmd](http://phpmd.org) stand for PHP Mess Detector.
```bash
brew install homebrew/php/phpmd
```
**[⬆ back to top](#table-of-contents)**


## PHP-CS-Fixer

[PHP-CS-Fixer](http://cs.sensiolabs.org) is a tool to automatically fix PHP coding standards issues.
```bash
brew install homebrew/php/php-cs-fixer
```
**[⬆ back to top](#table-of-contents)**


## Mou

[Mou](http://25.io/mou/) a markdown editor.
```bash
brew cask install mou
```
**[⬆ back to top](#table-of-contents)**


## Mysql

[Mysql](https://dev.mysql.com/doc/refman/5.7/en/) is an open source relational database management system.
```bash
brew install mysql
```
**[⬆ back to top](#table-of-contents)**


## FileZilla

[FileZilla](https://filezilla-project.org/) a FTP client.
```bash
brew cask install filezilla
```
**[⬆ back to top](#table-of-contents)**


## Istat-menus

[Istat-menus](https://bjango.com/mac/istatmenus/) is an advanced Mac system monitor for your menubar.
```bash
brew cask install istat-menus
```
**[⬆ back to top](#table-of-contents)**


## Git-Flow

[Git-Flow](https://github.com/nvie/gitflow) extensions to follow Vincent Driessen's branching model.
```bash
brew install git-flow
```
**[⬆ back to top](#table-of-contents)**


<hr>

<a name="osx-dev-setup-footnote-1">1</a>: https://github.com/nicolashery/mac-dev-setup

<a name="osx-dev-setup-footnote-2">2</a>: https://gist.github.com/jpantuso/1110217

<a name="osx-dev-setup-footnote-3">3</a>: http://apple.stackexchange.com/questions/93002/how-to-properly-update-git-on-mac/118128#118128

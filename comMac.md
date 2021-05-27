# MacOS

## Install

- _Note: Backup application files may include_
- _ApSp: - ~/Library/Application Support_
- _Pf: - ~/Library/Preferences_
- _Lc: - License File_

- Setup Apple Account
- Setting Preferences: Sharing, iCloud
- Download Documents BAckup for Support Files
- **App Setups**
  - [1Password](https://1password.com/) Pf+Login
  - [LaunchBar](http://www.obdev.com/products/launchbar/) ApSp+Pf
  - [VSCode](https://code.visualstudio.com) (Github Sync)
  - [Brave Browser](https://brave.com/) (Sync)
  - Mail
  - Finder
  - Craft
  - Tweetbot
  - Reeder (Pf+Login)
  - NordVPN (Login)
  - Safari Plugins: 1Password, Grammary, Reeder, AdGuard, Vimari
  - [Brave Browser](https://brave.com/) (Sync)
    - Plugins: AutoCookieDelete, Privacy Badger, uBlock Origin, Grammary, 1Password, Vimium, HTTPS everywhere #tag

### Install App Store Apps

- Audiobook Builder 2
- ToastDVD
- Magnet.app
- MS Office
- Meta.app
- Klib
- Pixelmator Pro.app
- DaisyDisk
- LiveReload.app
- Amphetamine.app
- Affinity Photo
- Affinity Designer
- Keynote
- Pages
- Numbers
- Kindle
- The Unarchiver

### Install Internet Apps

- [Resilio Sync](https://www.resilio.com/individuals/) Lc
- [Visual Studio Code](https://code.visualstudio.com/) Folders+Pf
- [Hazel](https://www.noodlesoft.com) +Rules+Lc
- [Forklift](https://binarynights.com) ApSp+Pf
- [Little Snitch](https://obdev.at/products/littlesnitch/download.html)
- [Micro Snitch](https://obdev.at/products/microsnitch/download.html)
- [Spotify](https://www.spotify.com/us/download/mac/)
- [Default Folder X](https://www.stclairsoft.com/DefaultFolderX/)
- [VLC](https://get.videolan.org/)
- [HandBrake](https://handbrake.fr/)
- [4K Download(Video, MP3, Instagram)](https://www.4kdownload.com/)
- [Affinity Publisher](https://store.serif.com/en-us/sign-in/?r&#x3D;%2Fen-us%2Faccount%2Fdownloads)
- [On1 Photo Raw](https://www.on1.com/account/products/)
- [Luminar](https://skylum.com/user/login)
- [Soulver 3](https://soulver.app/)
- [TripMode](https://tripmode.ch/)
- [Authy](https://authy.com/download/)
- [Houdah (Spot&Geo%CusShort)](https://www.houdah.com/) Lc
- [pCloud (MacFuse)](https://www.pcloud.com/)
- [Publicspace (Renamer Attributes Folder)](https://www.publicspace.net/ABetterFinderRename/)
- [TorBrowser](https://www.torproject.org/thank-you/) Bookmarks
- [Luminar](https://skylum.com)
- [Aurora HDR](https://skylum.com)
- [ON1 Photo RAW](https://www.on1.com)
- [balenaEtcher](https://www.balena.io/etcher/)
- [ApplePi Baker](https://www.tweaking4all.com/hardware/raspberry-pi/applepi-baker-v2/)
- [Dissenter Browser](https://dissenter.com/download) {AppSup}
- [Transmission.app](https://transmissionbt.com) {Find}
- [Logitech Driver](https://support.logi.com/hc/en-001/articles/360025298053)
- [VLC](https://www.videolan.org/vlc/index.html)
- [FastRawViewer](https://www.fastrawviewer.com)
- [Grammarly](https://www.grammarly.com/native/mac)
- [calibre](https://calibre-ebook.com/download_osx)
- [ff·Works](https://www.ffworks.net/download.html)
- [Plex Media Player](https://www.plex.tv/media-server-downloads/)
- [MakeMKV](https://www.makemkv.com/download/)
- [Marked](https://marked2app.com/)
- [Topaz Labs (Sharp Denoise)](https://topazlabs.com/)
- [qBittorrent](https://www.fosshub.com/qBittorrent.html)
- [Cryptomator](https://cryptomator.org/downloads/mac/thanks/)
- [Lemke Software: GraphicConverter](https://www.lemkesoft.de/en/products/graphicconverter/)
- [Skype](https://www.skype.com/en/)
- [Discord](https://discord.com/)
- [VeraCrypt (MacFuse)](https://www.veracrypt.fr/en/Downloads.html)
- [GPG Suite](https://gpgtools.org/)
- [Bisq](https://bisq.network/downloads/)
- [Exodus](https://www.exodus.io/)
- [Daedalus Wallet](https://daedaluswallet.io/)
- [Ledger](https://www.ledger.com/)

### Install CLI

- Copy Meslo Fonts into /System/Library/Fonts
- [iTerm2](https://iterm2.com/) ApSp+Pf+Profiles
- Install [homebrew](https://brew.sh): `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
- Install iTerm Tools: iTerm2->iTerm2->Install Shell Integration
- Install Zsh: `brew install zsh`
- Install Zsh: `zsh-completions`
  - Notes after everything is setup
  - To activate these completions, add the following to your .zshrc:  fpath=(/usr/local/share/zsh-completions $fpath)
  - You may also need to force rebuild zcompdump: `rm -f ~/.zcompdump; compinit`
  - If you receive "zsh compinit: insecure directories" run this: `chmod go-w '/usr/local/share'`
Install [mosh:](https://mosh.org) `brew install mosh`
  - Allow mosh through firewall
    - `sudo /usr/libexec/ApplicationFirewall/socketfilterfw --add /usr/local/Cellar/mosh/1.3.2_10/bin/mosh-server`
    - `sudo /usr/libexec/ApplicationFirewall/socketfilterfw --unblockapp /usr/local/Cellar/mosh/1.3.2_10/bin/mosh-server`
    - [Link](https://github.com/blinksh/blink/issues/11)
Install [fzf](https://github.com/junegunn/fzf): `brew install fzf`
  - setup `$(brew --prefix)/opt/fzf/install`
- Install [oh-my-zsh](https://ohmyz.sh) `sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`
- Install [Powerline Theme](https://github.com/romkatv/powerlevel10k) `git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/themes/powerlevel10k`
  - Change theme in .zshrc to `ZSH_THEME="powerlevel10k/powerlevel10k` in ~/.zshrc.
  - On the first run, Powerlevel10k configuration wizard will ask you a few questions and configure your prompt.
  - turn on instant prompt, quiet mode.
- Install [Tmux](https://www.ocf.berkeley.edu/~ckuehl/tmux/) `brew install tmux`
  - Install tmux plugin managar (Should be backup files)
  - `git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm`
- Install (Maybe) [VIM] `brew install vim`
- Install [Neovim](https://neovim.io/) `brew install neovim`
- Move Files from Backup/Root.zip into Root
- These Should be done
  - Add plugins to zshrc (should already be there)
    - Install Autosuggestions`git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions`
    - Install Syntax-Highlighting `git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting`
- Intall [Git](https://git-scm.com/): `brew install git`
  - Config Git
    - `git config --global push.default simple`
    - `git config --global user.name "user_name"`
    - `git config --global user.email "email_id"`
    - `git config --global pull.ff only` change how git pulls
  - Config Github Login
    - [Generate ssh key](https://docs.github.com/en/free-pro-team@latest/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
    - `ssh-keygen -t ed25519 -C "your_email@example.com"`
      - Hit enter to set Default location
      - Hit enter to set no paraphrase
    - Paste public key to github [website](https://github.com/settings/keys)
  - If you want credentials temporarily stored `git config --global credential.helper 'cache --timeout 3600'`
  - If you want permanent credentials do this before push `git config --global credential.helper store (first time only)`
  - Change Port
    - Check Old port: `ssh -T git@github.com`
    - Check New port: `ssh -T -p 443 git@ssh.github.com`
    - Create file: ~/.ssh/config
    - Add
        >Host github.com
        >  Hostname ssh.github.com
        >  Port 443
    - Check it see if works: `ssh -T git@github.com`
- Download Git repos into ~/Git Folder
- Setup ssh Keys
  - Create key: `ssh-keygen -t rsa`
    - rsa is the name of the key pair
    - Hit Enter on all commands
  - Copying Your SSH Public Key to a Web Server: `ssh-copy-id -i ~/.ssh/id_rsa.pub username@yourwebserver.com`
  - Protect Key
    - `sudo chmod 600 ~/.ssh/id_rsa`
    - `sudo chmod 600 ~/.ssh/id_rsa.pub`

Waiting

- Install Github CLI `brew install gh`

### MacMini Apps

Soundsource
Logtitech _GHub_
Logitech Capture
[i1Studio](https://xritephoto.com/ph_product_overview.aspx?action&#x3D;support&amp;id&#x3D;2458)
FF-works (FFmpeg) (Mac)
[Tweaking4All-ApplePiBaker](https://www.tweaking4all.com/hardware/raspberry-pi/applepi-baker-v2/)
[balenaEtcher](https://www.balena.io/etcher/)
[MakeMKV](https://www.makemkv.com/)
Calibre
[calibre](https://calibre-ebook.com/download)
[PowerPanel](https://www.cyberpowersystems.com/products/software/power-panel-personal/)
[VMware](https://maintenance.vmware.com/info6.html)

## Configuration

### Startup Items

- Log in items in the “Users and Groups” preference pain.
- Applications that run on Startup:
  - (User or System)_Library_StartupItems
  - (User or System)_Library_LaunchDaemons
  - (User or System)_Library_LaunchAgents/
- Applications that run on a set schedule:
  - Check your crontab with terminal: crontab -l
- Check Kernel Extensions:
  - In the command line: kextstat
- Check Login and Logout Hooks
  - defaults read com.apple.loginwindow LoginHook
  - defaults read com.apple.loginwindow LogoutHook
  - or use terminal: _usr_libexec_PlistBuddy -c Print ~_Library_Preferences_com.apple.dock.plist (Dock options menu)

## Shortcuts

### Reminders

- Command I or double click to edit to edit
- spacebar to mark completed
- two finger swipe to switch between lists

### Notes

- Two-finger swipe for Notification Center
- To reveal Notification Center swipe two fingers from physically off your trackpad on to it. It takes a bit of practice but becomes a very useful way to check your emails and Twitter notifications.
- Reminders will automatically convert day and time information to a date-based reminder
- Add return to owner message on lock screen
- System Prefs / Security & Privacy / Show message;
- Add send from shortcut
- System Pref / Keyboard / Application shortcuts / Mail / “Name of Mail account” / Shortcut key
- Spotlight quere syntax
- Use Function Plus Option to access shortcuts

### Pixelmator

- Quartz Composer: These filters were created using Quartz Composer, a tool included for free with every Mac, in Apple’s developer tools. Quartz Composer is a great application, allowing the creation of visual compositions very easily, while harnessing the graphical power of Quartz itself. While a first approach may be daunting because of the unusual programming method, after learning the basics you can very quickly discover new possibilities, and create interesting compositions with ease.
- How to install: To install these filters, copy them into the _Library_Compositions/ folder, creating it if necessary. The filters will appear in Pixelmator the next time it is relaunched, and other applications that load Quartz filters should be able to use these as well.

### Finder

- ⌘ ⇧Y - Full Screen Quick-view (multiple files too for slideshow)
- Space - Quick-view
- ⌘` Cycle Through Windows
- ⌘⌫ Send to Trash
- ⇧⌘⌫ Empty trash
- Option click menu bar item form more info
- Use Option or option/shift for resizing windows
- Shift / Option for incrementally adjust brightness and volume
- option/command V to move file that was copied.
- Default width of the Finder’s columns can be changed by
- option-dragging the column handle to your preferred widthΩ

### System

- ⌘⇥ Application Switcher (⌘Q Quit)
- ⌘⌫ Deletes Line
- ⌥⌫ Deletes front word
- fn⌥⌫ Deletes back word
- ⌫ deletes back character
- fn⌫ deletes forward character
- Save Dialog Shortcuts
- ⌘D or ⌘⇧D Desktop
- ⌘⇧H Home Folder
- ⌘⇧A Application
- ⌘⇧N New Folder
- ⌘⇧. Toggle Hidden File
- ⌘⇧G Path dialog

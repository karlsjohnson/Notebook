# Install

Install **Homebrew**

- Install **[homebrew](https://brew.sh)**: `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`
- Install **Cask**:_(extends Homebrew to OS X applications)_ `brew install cask`
- Install **brew software** `brew install <app>`

Install **iTerm2**

- Install **iTerm2** `brew cask install iterm2`
- Copy **iTerm2 Apps Files**
  - ==Need More Information==
- Install iTerm Tools: iTerm2->iTerm2->Install Shell Integration

Install **Zsh**

- **zsh**
- ==How to Install?==
- **zsh-completions**
  - ==How To Install?==
  - To activate these completions, add the following to your .zshrc:  fpath=(/usr/local/share/zsh-completions $fpath)
  - You may also need to force rebuild zcompdump: `rm -f ~/.zcompdump; compinit`
  - If you receive "zsh compinit: insecure directories" run this: `chmod go-w '/usr/local/share'`

Install **fzf**

- **fzf** `brew install fzf`
  - setup `$(brew --prefix)/opt/fzf/install`
  - Link .fzf.zsh `ln -s ~/Documents/Code/Root/fzf.zsh ~/.fzf.zsh`

Install **On-my-zsh**

- Install [oh-my-zsh](https://ohmyz.sh) `sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`
- Link zshrc `ln -s ~/Documents/Code/Root/zshrc.sh ~/.zshrc`
- Link zlogin `ln -s ~/Documents/Code/Root/zshrc ~/.zshrc`
- Link zlogout `ln -s ~/Documents/Code/Root/zshrc ~/.zshrc`
- Link zprofile `ln -s ~/Documents/Code/Root/zshrc ~/.zshrc`
- Link zshenv `ln -s ~/Documents/Code/Root/zshrc ~/.zshrc`
- Install Powerline Theme `git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/themes/powerlevel10k`
- Change theme in .zshrc to `ZSH_THEME="powerlevel10k/powerlevel10k` in ~/.zshrc.
- On the first run, Powerlevel10k configuration wizard will ask you a few questions and configure your prompt.
  - turn on instant prompt, quiet mode.
- Link .p10k.zsh `ln -s ~/Documents/Code/Root/p10k.zsh ~/.p10k.zsh`
- Link oh-my-zsh.sh `ln -s ~/Documents/Code/Root/oh-my-zsh.sh ~/.oh-my-zsh/oh-my-zsh.sh`
- Copy Root/Fonts into /System/Library/Fonts
- Install Autosuggestions`git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions`
- Install Syntax-Highlighting `git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting`
  - Add plugins to zshrc (should already be there)
- Move all files to ilCloud, name ROOT variable

Instal **Tmux**

- Setup **Tmux**
  - Install `brew install tmux`
  - Link .tmux.conf `ln -s ~/Documents/Code/Root/tmux.sh ~/.tmux.conf`
  - Install tmux plugin managar
    - `git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm`

==Todo MacMini Below==

Install **Vim**

- Install **Neovim**
  - Install `brew install neovim`
  - Link Config Folder
    - Link .vim `ln -s ~/Documents/Code/Root/config/ ~/.config`
    - Link .vim `ln -s ~/Documents/Code/Root/local/ ~/.local`

- Install Github CLI
  - brew install gh

Install **Node**

- Install Node Package manager


Install and Setup **Ruby & Gem**

- Setup RubyGems
  - ==Work in progress, stalled on errors to get mdless to run==
  - ==Start Over==
  - [Download RubyGems](https://rubygems.org/pages/download)
  - Install ruby: `brew install ruby`
  - Install Ruby Gems: `brew install brew-gem`
    - Check `export PATH="/usr/local/opt/ruby/bin:$PATH"` in in the szshrc
- [Gems:](https://rubygems.org/pages/download)
  - Update: `gem update —system`
  - Already installed (With ruby)
  - Check version: `ruby —version`, `gem —version`
  - list commands: `gem`
- [Ruby Version Manager:](https://rvm.io/)
- Work out rubygems with rvm
  - command: `which -a ruby` which command are you using and `ruby -v`, what version
-Work on setting up ruby gems and running them
  - [RubyGems](https://rubygems.org/pages/download)
  - [mdless](https://brettterpstra.com/projects/mdless/)
- Link: [mdless](https://brettterpstra.com/projects/mdless/)
- Install: `gem install mdless`
  - if error, update gems: `https://rubygems.org/pages/download`
- Usage: `mdless [options] path or cat [path] | mdless`

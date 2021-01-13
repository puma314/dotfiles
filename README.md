## Setting up iTerm2 with Agnoster:

* Download iTerm2
* Download oh-my-zsh [https://ohmyz.sh/], this will change the `.zshrc`
* Change theme from robbyrussel to agnoster in the `.zshrc`
* Use warhol plugin for colored folders [https://github.com/unixorn/warhol.plugin.zsh]
* Download powerline fonts and install them:
```
git clone https://github.com/powerline/fonts.git --depth=1
cd fonts
./install.sh
cd ..
rm -rf fonts
```
* Set fonts in iTerm2 in both non-acsii and normal to powerline (Preferences/Profiles/Text/Font/Meslo LG S DZ for Powerline), make sure "Use a different font for non-ASCII text is unchecked)
* Make sure that pyenv is still correctly setup in the `.zshrc`:
```
echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zshrc
echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zshrc
echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n  eval "$(pyenv init -)"\nfi' >> ~/.zshrc
```
* Add `DEFAULT_USER=$USER` to `.zshrc` to get rid of `user@computer` part of prompt
* iTerm2: Uncheck Preferences/Appearance/Dimming/Dim inactive split panes
* iTerm2: Preferences/Profiles/Colors/Color Presents/Solarized Dark preset

## Setting up vim with .vimrc (and vundle)
* `cp ~/dotfiles/.vimrc ~/.vimrc`
* Install vundle: [https://github.com/VundleVim/Vundle.vim]
`git clone https://github.com/VundleVim/Vundle.vim.git ~/.vim/bundle/Vundle.vim`
* Launch `vim` and run `:PluginInstall`

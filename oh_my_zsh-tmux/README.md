
---
# Using the terminal multiplexer "TMUX"
Hit the Prefix key defined as "Ctrl+B" before each of the follwing command:-
```bash
1. % - for vertical splitting of the terminal into two terminals
2. " - for horizontal splitting of the terminal into two terminals
3. Arrow keys - to switch between terminals
4. z - to zoom in on the selected terminal. (Note: Use the same command to zoom out)
5. Hold the Ctrl key - resize the terminal
6. Spacebar - to switch between different arrangements of the terminals
7. { - to move the selected terminal to the left
8. } - to move the selected terminal to the right
9. c - to open a new window in TMUX
10. Ctrl+B follwed by **whatever your window's number is** - Will switch to that particular window in TMUX
11. [ - to enter scroll mode. Use arrow keys or the mouse after entering scroll mode to scroll. Hit "q" to exit scroll mode.

```

All the commands for TMUX can be found here: https://linux.die.net/man/1/tmux

## Installing and configuring oh-my-zsh
To install oh-my-zsh:-
```
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
1. Installing auto-suggestions
```
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
plugins=(zsh-autosuggestions)
```
2. Install fzf. fzf is an interactive fuzzy file search tool on the command-line. It is fast and powerful. 
Refer - https://jdhao.github.io/2018/11/05/fzf_install_use/
```
git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
~/.fzf/install
```


## Configuring tmux
Add the following line in your .zshrc file:-
```
subl .zshrc #to open .zshrc file
```
Add the following line:-
```
# Automatically start a tmux session upon logging in.  
ZSH_TMUX_AUTOSTART="true"  
```
Then, add tmux to the list of plugins further down in the .zshrc file as shown:-
```
plugins=(  
  git  
  sublime  
  tmux  
  zsh-autosuggestions
)  
```
Also, install zsh autosuggestions using this link:-
https://github.com/zsh-users/zsh-autosuggestions/blob/master/INSTALL.md

To be edited...
```
tmux show -g | cat > ~/.tmux.conf
subl ~/.tmux.conf #using sublime to open the hidden file .tmux.conf
Adding panes
```

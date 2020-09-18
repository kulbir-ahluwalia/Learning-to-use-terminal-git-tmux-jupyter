# Git commands
1. You can make branches for different versions of a repo, there is also the option to merge the branch into the master branch.
2. You can fork a repo to get a exact same copy of the repo in your account, and then initiate a pull request (PR) to transfer your changes into the parent repo.
3. I have made a separate branch with all my changes in my forked repo, But how do I pull your original repo to my forked repo?
```
git remote -v   #to view remotes at present
git remote add upstream https://github.com/kanishkaganguly/shadowevents.git   #to add the repo "shadowevents" with the remote name "upstream".
#you could have also named it "test_name"	
# then, view all the remote repos again to see the changes using:
git remote -v 
```
To see the changes ina file:
```
git log -p <file name>
```

 
official source for managing remote repositories :
 https://docs.github.com/en/github/using-git/managing-remote-repositories



# About Oh-my-zsh
**Oh-my-zsh** - Alternative for bash    
Note for zsh - Install PowerLevel10k theme, zsh-syntax-highlighting, zsh-autosuggestions enabled, fzf (Ctrl+R for searching previously entered commands, Ctrl+T for finding files, Alt+C for changing directory to some folder)  
**Make your terminal more productive** - https://medium.com/@ivanaugustobd/seu-terminal-pode-ser-muito-muito-mais-produtivo-3159c8ef77b2
## Install Sublime text
```
sudo apt update
sudo apt install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -
sudo add-apt-repository "deb https://download.sublimetext.com/ apt/stable/"
sudo apt update
sudo apt install sublime-text
```
## Install driver for Wifi: Killer AX1650 In Debian/Ubuntu 16.04+
https://support.killernetworking.com/knowledge-base/killer-ax1650-in-debian-ubuntu-16-04/

## Install Pycharm and CLion
```
sudo apt update
sudo apt install snapd
#for Pycharm PE
sudo snap install pycharm-professional --classic	
#for PyCharm CE
sudo snap install pycharm-community --classic
#for CLion
sudo snap install clion --classic
```
## Install zsh
```
#First, in order to check if you're using zsh or bash:
echo $0
#to install zsh:-
sudo apt install zsh
```
# Install curl, git
```
sudo apt install curl
sudo apt-get install git
```

# Installing and configuring oh-my-zsh
To install oh-my-zsh:-
```
curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh | sh; zsh
sudo usermod --shell $(which zsh) $USER
```
1. Installing auto-suggestions
```
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```
2. Install fzf. fzf is an interactive fuzzy file search tool on the command-line. It is fast and powerful. 
Refer - https://jdhao.github.io/2018/11/05/fzf_install_use/
```
git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
~/.fzf/install
```
3. Installing syntax highlighting
```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```
## Adding the name of plugins in .zshrc
Open .zshrc using sublime text:
```
subl .zshrc
```
Add ```zsh-autosuggestions```,```fzf``` and ```zsh-syntax-highlighting``` in plugins=() so that it looks like:
```bash
plugins=(
	git
	zsh-autosuggestions
	fzf
	zsh-syntax-highlighting
	)
```
Save your .zshrc and then source it using:
```
source .zshrc
```
After you restart your terminal, you should see the effects of installing these plugins.
If not, log out and log back in.


## Installing PowerLevel 10K theme
```
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k
```

Add the line ```ZSH_THEME="powerlevel10k/powerlevel10k"``` in your .zshrc file.
Comment the ZSH theme that you had previously. In my case, it was ```ZSH_THEME="robbyrussell"```. Comment it. End result:
```bash
#ZSH_THEME="robbyrussell"
ZSH_THEME="powerlevel10k/powerlevel10k"
```
Configure the powerlevel10k theme from the terminal by choosing from the options that come up on the terminal.

## Using zsh with ROS
You have to execute the following commands to your .zshrc file to source the environment variables in your terminal:
```
echo "source /opt/ros/kinetic/setup.zsh" >> ~/.zshrc
source ~/.zshrc
```

## Uninstalling zsh and oh-my-zsh
```
#Run the following command in the terminal to uninstall oh-my-zsh
uninstall_oh_my_zsh

# switch default shell to bash from zsh
chsh -s /bin/bash ksa

#then uninstall zsh
sudo apt-get --purge remove zsh

#restart terminal
```

# Using the terminal multiplexer "TMUX"
Install it using:
```
sudo apt-get install tmux
```
To start tmux, just enter tmux in the terminal and press enter.
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


# Configuring tmux
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

# Enabling pane change, scroll using mouse 
```
subl .tmux.conf 
#write the following line in the .tmux.conf file
set-option -g mouse on #this will enable scrolling and pane selection, but then you need to press shift to select text using the mouse
#then save the file, come back to the terminal, then:
tmux source-file ~/.tmux.conf
```
To be edited...
```
tmux show -g | cat > ~/.tmux.conf
subl ~/.tmux.conf #using sublime to open the hidden file .tmux.conf
Adding panes
```

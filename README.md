Credits: I am thankful to my friends Sandeep Kota and Vishnu Dorbala for their support and guidance. The following work largely consists of tips and tricks I learnt from them.


```
Note:-
1. To align a window to the left half of the screen, use Ctrl+Windows+left arrow 
2. To align a window to the right half of the screen, use Ctrl+Windows+right arrow 
3. You can use .conf files to configure applications like the Z shell or TMUX. ".conf" stands for a **configuration** file used in Ubuntu in this case.
```

# Helpful tips and commands for using the terminal
1. For copying in terminal, use Ctrl+Shift+C. 
2. For pasting in terminal, use Ctrl+Shift+V.
3. Use Tab for auto completion wherever possible.
---
4. Use workspaces to increase productivity. Shift windows to different workspaces using Ctrl+Shift+Alt+arrow keys.
5. Switch between workspaces using Ctrl+Alt+arrow keys.
6. To enable workspaces, go to System settings>Appearance>Enable workspaces.
---
7. A period "**.**" as the first character in the file name indicates that it’s a hidden file. For example, **~/.tmux.conf** is a hidden file at the location **~**.
8. **~** refers to the path **/home/kulbir**
9. To check your working directory, use the command **pwd**. It will tell you the path of the current working directory.
10. You probably know this, but yes, I will write it. The shortcut to open the terminal is **Ctrl+Alt+T**. 

# For copying using the terminal
Using the copy command with Recursive search (-R for recursive and -i for interactive):-
1. The path from where the file is **copied from** is written first.
2. The path where the file is **copied to** is written afterwards.
3. Use sudo to get permissions for copying as shown:-

```bash
sudo cp -Ri Source_Folder Destination_Folder
sudo cp -Ri ~/Downloads/tmux.conf  /usr/share/doc/tmux/examples
```

# For copying files using GUI:-
```bash
gksu nautilus
```


---
# Basic writing and formatting syntax for GitHub
- https://help.github.com/en/github/writing-on-github/basic-writing-and-formatting-syntax
1. Double space is used for changing the line
2. Format for comments:-
```
<!--Insert your comment here-->
```
3. To insert an image, first upload the image to the repo and then:-
```
<img src= "name of the image with extension" class="img-responsive" alt=""> </div>
```
---

# Using git to setup a repository for our python files

Installing git:-   
```bash
sudo apt-get install git
```

Setup username:-    
```bash
git config --global user.name "kulbir-ahluwalia"
```  

Setup email:-  
```bash
git config --global user.email "kulbir@terpmail.umd.edu" 
```  

Make a directory in your PC:-  
```bash
cd Documents/  
mkdir OOP
cd OOP/ 
```
---
Helpful tip:-
When you create the repository on GitHub don't provide any description or initialise it with a README.md file. 
So that you get the following menu with all the commands for setting the repo up:-
<!--For displaying image in GitHub-->

<img src= "menu_repo.png" class="img-responsive" alt=""> </div>


---

To create a new repository on the command line:-  
```bash
#to create a readme file   
echo "# OOP_Python" >> README.md    

# to initialize empty git repository in the directory /home/kulbir/Documents/OOP_Python/.git/   
git init   

#to add the readme file   
git add README.md   

#to commit your file and save your changes  
#The comment regarding the purpose of the commit is written in double quotes  
git commit -m "first commit"    

#to add the remote origin, link the local directory on PC with the GitHub directory  
git remote add origin https://github.com/kulbir-ahluwalia/OOP_Python.git   

#to push your changes  
git push -u origin master     
```

### Adding new files using git
Create a new file in the directory /home/kulbir/Documents/OOP_Python:-  

```bash
nano OOP_practice_instances1.py 
```
To add the new file:-  
```
 git add OOP_practice_instances1.py  
 git add *    #to add all the files in the current working directory
 git add .    #alternate way to add all the files in the current working directory
 git add --all  #to add all files in the folder irrespective of your current working directory
 git add --A    #alternate way to add all files in the folder irrespective of your current working directory

```
To commit the file and save the changes with a custom comment describing the changes:-  

```
git commit -m "OOP_python_instances"
```
To add the remote origin, link the local directory on PC with the GitHub directory (If you haven't already done it) :-  
```
git remote add origin https://github.com/kulbir-ahluwalia/OOP_Python.git 
```
To push your changes:- 
Note: When you use the following command, the terminal will retun the message "1 file changed, 1 insertion(+) "
```
git push -u origin master  
```
---

### Removing files using git 

To remove the file from the git repository and from the directory on your system:-
Note: "rm" stands for "remove". When you use the following commands, the terminal will retun the message "1 file changed, 1 deletion(-)"

```
git rm OOP_practice_instances1.py  
git commit -m "deleted OOP_practice_instances1.py"
```
---
To remove the file only from the git repository and not from the directory on your system:-
```
git rm --cached OOP_practice_instances1.py
git commit -m "deleted OOP_practice_instances1.py"
```

To push changes to the existing repository on GitHub:-
```bash
git remote add origin https://github.com/kulbir-ahluwalia/OOP_Python.git 
git push -u origin master 
```

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

# Installing Jupyter notebook
This should launch the jupyter notebook with the option to create new files in python 2 and python 3:-
```
sudo apt install python-pip
sudo apt install python3-pip
pip install notebook
pip install jupyter
pip3 install jupyter
sudo -H pip install jupyter
jupyter notebook #to launch the jupyter notebook
```
(Some commands maybe redundant but this is what worked...)

---
# References
1. For git commands - https://rogerdudler.github.io/git-guide/
2. For using git and GitHub - https://youtu.be/SwK2dPFXhpU
3. For TMUX - https://youtu.be/Lqehvpe_djs
4. For git commands with examples - https://rubygarage.org/blog/most-basic-git-commands-with-examples


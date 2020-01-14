# Helpful tips and commands for using the terminal

Note:-
1. For copying in terminal, use Ctrl+Shift+C. 
2. For pasting in terminal, use Ctrl+Shift+V.
3. Use Tab for auto completion wherever possible.
4. Use workspaces to increase productivity. Shift windows to different workspaces using Ctrl+Shift+Alt+arrow keys.
5. Switch between workspaces using Ctrl+Alt+arrow keys.
6. To enable workspaces, go to System settings>Appearance>Enable workspaces.
7. A period as the first character in the file name indicates that it’s a hidden file. For example, **~/.tmux.conf** is a hidden file at the location **~**.
8. ~ refers to the path **/home/kulbir**
9. To check your working directory, use the command **pwd**. It will tell you the path of the current working directory.
10. You probably know this, but yes, I will write it. The shortcut to open the terminal is **Ctrl+Alt+T**. 

Using the copy command with Recursive search (-R for recursive and -i for interactive):-
Note:-
1. The path from where the file is **copied from** is written first.
2. The path where the file is **copied to** is written afterwards.
3. Use sudo to get permissions for copying
```
sudo cp -Ri Source_Folder Destination_Folder
sudo cp -Ri ~/Downloads/tmux.conf  /usr/share/doc/tmux/examples
```

For copying using GUI:-
```
gksu nautilus

```
# Using git to setup a repository for our python files

Installing git:-   
```sudo apt-get install git```

Setup username:-    
```git config --global user.name "kulbir-ahluwalia"```  
Setup email:-  
```git config --global user.email "kulbir@terpmail.umd.edu"```  

Make a directory in your PC:-  
```cd Documents/  
mkdir OOP
cd OOP/  
```
To create a new repository on the command line:-  
```
#to create a readme file   
echo "# gittest" >> README.md   

# to initialize empty git repository in the directory /home/kulbir/Documents/OOP/.git/   
git init   

#to add the readme file   
git add README.md   

#to commit your file and save your changes  
#The comment regarding the purpose of the commit is written in double quotes  
git commit -m "first commit"    

#to add the remote origin, link the local directory on PC with the GitHub directory  
git remote add origin https://github.com/kulbir-ahluwalia/OOP_Python_Practice.git  

#to push your changes  
git push -u origin master     
``` 

To push an existing repository from the command line:-
```
git remote add origin https://github.com/kulbir-ahluwalia/OOP_Python.git    
git push -u origin master  
```





# OOP_Python  
OOP practice using Python  

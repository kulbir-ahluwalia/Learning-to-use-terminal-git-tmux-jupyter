# Using git to setup a repository for our python files
Note:-
1. For copying in terminal, use Ctrl+Shift+C. 
2. For pasting in terminal, use Ctrl+Shift+V.
3. Use Tab for auto completion wherever possible.
4. Use workspaces to increase productivity. Shift windows to different workspaces using Ctrl+Shift+Alt+arrow keys.
5. Switch between workspaces using Ctrl+Alt+arrow keys.
6. To enable workspaces, go to System settings>Appearance>Enable workspaces.



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
echo "# gittest" >> README.md  #to create a readme file  
git init # to initialize empty git repository in the directory /home/kulbir/Documents/OOP/.git/  
git add README.md  #to add the readme file  
git commit -m "first commit"  #to commit your file and save your changes, comment regarding the purpose of the commit in double quotes  
git remote add origin https://github.com/kulbir-ahluwalia/OOP_Python.git  #to add the remote origin, link the local directory on PC to GitGub directory
git push -u origin master   #to push your changes
``` 

To push an existing repository from the command line:-
```
git remote add origin https://github.com/kulbir-ahluwalia/OOP_Python.git  
git push -u origin master
```





# OOP_Python  
OOP practice using Python  

# Lab Report 1
How to log into a course-specific account on ieng6: <br>
## Installing VSCode <br>
- Use the link [VSCode Windows Install](https://go.microsoft.com/fwlink/?LinkID=534107) to Download VSCode to your computer. When it has been downloaded, and the installer has been run, it should open to look like this:
![Image](install-vscode.jpg)
## Remotely Connecting <br>
- In order to connect using a course-specific account, you must first dowload [Install OpenSSH](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse) <br>
- Next, use [UCSD Account Lookup](https://sdacs.ucsd.edu/~icc/index.php) to find your username for your specified course. They will be listed under Additional Accounts (highlighted in yellow).
![Image](find-account.jpg)
- Make a file in VSCode and open a new terminal. Then use the command $ ssh csdp15lsp22anb@ieng6.ucsd.edu. Note that the part before the @ieng6.ucsd.edu matches my account name as seen in the previous image (underlined in pink).
- If this is your first time attempting to log in, you will receive a message asking you to confirm that you want to log in. You will do this by typint $ yes
- 
## Trying Some Commands <br>
## Moving Files with scp <br>
## Setting an SSH Key <br>
## Optimizing Remote Running <br>
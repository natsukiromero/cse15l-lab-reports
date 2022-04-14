# Lab Report 1
How to log into a course-specific account on ieng6: <br>
## Installing VSCode <br>
- Use the link [VSCode Windows Install](https://go.microsoft.com/fwlink/?LinkID=534107) to download VSCode to your computer. When it has been downloaded, and the installer has been run, it should open to look like this: <br>
![Image](install-vscode.jpg)
  
## Remotely Connecting <br>
- In order to connect using a course-specific account, you must first dowload [Install OpenSSH](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse).
- Next, use [UCSD Account Lookup](https://sdacs.ucsd.edu/~icc/index.php) to find your username for your specified course. It will be listed under Additional Accounts (highlighted in yellow). <br>
![Image](find-account.jpg)
- Make a file in VSCode and open a new terminal. Then use the command ```ssh cs15lsp22anb@ieng6.ucsd.edu```. Note that the part before the @ieng6.ucsd.edu matches the course specific account name as seen in the previous image (underlined in pink).
- If this is your first time attempting to log in, you will receive a message asking you to confirm that you want to log in. You will do this by entering ```yes```.
- The system will then prompt you for a password. This password is the same as your global password (aka the one you use for AD Login). Note that for security purposes, when you type into the password field there will be nothing to indicate that it is being typed, not even ***.
- If successful, you should see the message depicted below: <br>
![Image](login.jpg)
  
## Trying Some Commands <br>
- Now that you are remotely logged in, you may try some of the various Unix commands- these will respond with the corresponding results from the other computer and not yours!
- You should play around with the commands to familiarize yourself with them, but some commands to try are: ```cd```, ```ls```, ```pwd```, ```mkdir```, ```cp```, and ```cat```. Try different variations of them as well (e.g. ```cd``` and ```cd~```, or try ```cd``` starting from different folders). <br>
![Image](commands.jpg)
  
## Moving Files with scp <br>
- The command ```scp``` is very useful to programmers, as it allows them to copy files back and forth between their own computer and the one they are remotely logged into. It is important to note that this command is always run on the programmers own computer (make sure you are logged out of ssh(```logout```)).
- Create a file WhereAmI.java on your computer, and then use javac and java to compile and run it to ensure it works. Then use the command ```scp WhereAmI.java cs15lsp22anb@ieng6.ucsd.edu:~/```. (You will have to enter your password.)
- Using the ```ls``` command should reveal that WhereAmI.java has been copied to the ieng6 computer. Log into the the ieng6 server, and you will then be able to run javac and java on file on the ieng6 computer. <br>
![Image](scp.jpg)
  
## Setting an SSH Key <br>
- It can be annoying to type out your password so often, so the command ```ssh-keygen``` was created to help. This command creates a pair of keys (one on the client(your) side and one on the server(ieng6) side). These keys together form an alternate method of authentification.
- On your own computer, run ```ssh-keygen```. You will be asked where to save the key, and you should return the location in the paranthesis of the prompt (in blue text). <br>
![Image](key-location.jpg)
- Next, you will be asked to enter a passphrase, with the option to leave the passphrase blank. For Lab 1, we were instructed to leave it blank. You will also need to enter it a second time for confirmation. <br>
![Image](make-key.jpg)
- We now need to copy the key onto the server, so log in and use the command ```mkdir .ssh```.
- Logout and use the command ```scp \Users\natsuki/.ssh/id_rsa.pub cs15lsp22anb@ieng6.ucsd.edu:~/.ssh/authorized_keys``` (using your own location and account name of course) to copy the file to your computer. Once this step is complete, you should be able to ```ssh``` and ```scp``` without a password (assuming your passphrase is empty). <br>
![Image](key-last-steps.jpg)
- Please note that this image does not contain the ```mkdir .ssh``` step
  
## Optimizing Remote Running <br>
- In order to make editing and copying files as easy as possible, there are a few shortcuts we can use.
- Writing a command in quotes at the end of the ssh login command will prompt the computer to remotely login, execute the command, then log back out.
- Multiptle commands can be run in the same command line using semicolons. <br>
![Image](semicolon.jpg)<br>
<br>
[return to home page](index.html)
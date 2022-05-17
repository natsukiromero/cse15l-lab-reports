# Lab Report 3
More work with ieng6 <br>

## Streamlining ```ssh``` Configuration <br>
By creating a file ```.ssh/config``` and entering the necessary information, it is possible to create a shortcut for ```ssh```ing into remote accounts. Similar to how the id_rsa allows us to skip typing in our passcode, this file will eliminate the need to type out our full username. Therefore, the command goes from ```ssh cs15lsp22anb@ieng6.ucsd.edu``` to ```ssh ieng6```- much simpler and easier! <br>
![Image](config.jpg)<br>
![Image](ssh-login.jpg) <br>
This also works for any time where we would've had to type out our remote account, such as ```scp```ing a file. <br>
![Image](scp.jpg)<br>

## Setup Github Access from ieng6 <br>
- ```ssh``` key stored in github: <br>
![Image](github-ssh.jpg) <br>
- ```ssh``` key on user account: <br>
![Image](id-file.jpg) <br>
In order to commit and push to github directly from outhome computers, we must use some sort of token-based authentification systems like ```ssh``` keys. Storing them on github and the computer has the same effect as storing id_rsa keys on ieng6 and the home computer- allows us to login automatically. <br>
- commit from ieng6: <br>
The necessary commands to commit and push a file, in this case lab-report-3-week-6.md, are as follows: <br>
> ```git add lab-report-3-week-6.md``` <br>
> ```git commit``` <br>
> ```git push``` <br>

![Image](commit.jpg) <br>
After entering ```git commit```, the following text will prompt you to enter a message to accompany your commit. The instructions to use it are as follows: <br>
> type message <br>
> press 'esc' <br>
> type ":wq" and hit enter <br>

The commit message will be added, and this text will disappear.

![Image](commit-message.jpg) <br>

- [link to commit](https://github.com/natsukiromero/cse15l-lab-reports/commit/a8797473361ae5a3f2635605292868e1fbccf1bb) <br>

## Copy whole directories with ```scp -r``` <br>
- using ```scp -r``` to copy markdown-parser to ieng6
![Image](3.1.jpg) <br>
- logging into ieng6 and running the tests
![Image](test.jpg) <br>
- combining it all into one line:
![Image](scp-r.jpg) <br>
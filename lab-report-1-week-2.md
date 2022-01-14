# Lab Report #1 - Week 2

## Installing VSCode
![Image](/images/VSCode.png)
* Go to the visual studio code website and find the download page
* Based on what computer you're using, click download
* Once the download is finished, unzip the download folder and open the application. Once you open the application, it should look something like the picture below:
![Image](/images/VSCodeOpen.png)

## Remotely Connecting
![Image](/images/RemoteConnect.png)
* Look up your CSE15L account here: [Link](https://sdacs.ucsd.edu/~icc/index.php)
* Open the terminal on VSCode and enter the following code below, replacing "zz" with the letters of your course-specific account
`ssh cs15lwi22zz@ieng6.ucsd.edu`
* Once it asks if you are sure you want to continue connecting, say yes
* Enter your TritonLink password (you may need to enter the password multiple times)

## Trying Some Commands
* Below is a list of commands you should know:
```
cd - changes directory with a specific path
cp - copys files
ls - lists contents of a directory
mv - moves files and/or renames files
rm - deletes files
mkdir - creates a directory
exit - logs out of linux
```
* Here's an example of using `ls -al`, which prints out every single file and directory that is running in the current directory, and shows which files that people can access and when it was last updated:
![Image](/images/TryingSomeCommands.png)

## Moving Files with scp
* The scp code command copies a local file from your computer (the client), and transfers the copy to the server
* Make sure you are on your computer's terminal and not the server
`scp <file name> <user name>`
* The command will prompt you to enter your TritonLink password, but once the file is fully transferred, it should look like this:
![Image](/images/SCP.png)
* Once the file is fully transferred, log back into the server and enter the `ls` command
* You should be able to see the file in the server. Below is a screenshot of a file being successfully copied over from the client to the server:
![Image](/images/SCP-LS.png)

## Setting an SSH Key
* On client, run the following command line below:
`ssh-keygen`
* This command created two new files on your system; one the private key (in a file id_rsa) and other for the public key (in a file id_rsa.pub), stored in the .ssh directory on your computer
* When it asks for your password, **press enter instead of typing in your tritonlink password**. Doing this will allow you to log into the server without entering your tritonlink password, which can be tedious at times
* Now we will copy the public key into a .ssh directory. Log back into the server and type the following command:
`mkdir .ssh`
* Log back into the client and copy the following command:
`scp <key path> <username>:~/.ssh/authorized_keys`
* You should now be able to log onto the server without your password. Heres an example below:
![Image](/images/SSHKey.png)

## Optimizing Remote Running
* There are commands that you can utilize to make your code run faster
* When you write a command after logging into the server, the command will automatically run it without having to type the command in a new line
`ssh <username> "<command>"`
* You can also run multiple commands at the same time by using a semicolon to separate them 
`ssh <username> "javac ARandomFile.java; java ARandomFile"`
* Below is an screenshot of mutiple commands running on the server:
![Image](/images/OptimizingRemoteRunning.png)

# Lab Report 1:How to log into a course specific account on *ieng6*

1. **Instaling VScode:**
First we will show you how to download VisualStudio Code. On your webbrowser you will need to open the visual studio website which can be done by following this link, [Visual Studio Code](https://code.visualstudio.com/). Once on the website you can choose the download that is best fit for the type of computer you have. Once pressing the download best fit for your operating system it will prompt you with instruction on how to download and install visual studio code for your specific operating system. Once you have completed there instructioon you would have completed the first step, **instaling VScode**. //inset image of visual studio code download and possible the app on desktop.
2. **Remotely Connecting:**
Now we can move onto the second step which is being able to remotely connect to a computer that is the CSE basement. First we will access the terminal which can be done by going to the top bar of your computer and pressing **Terminal** and then selecting **New Terminal**. Once the terminal has been opened you can type in the terminal, ssh cs15lsp22mm@ieng6.ucsd.edu, where mm is a placeholder for your own letters that is in your course-specific account. If this is your first time logging into the server you will receive a message as shown in the image; //Show
You only need to enter yes to get to the promot where it will ask for your password. Once you enter yes you will the be prompt to enter password you will then need to enter the password. Keep in mind you will not be able to see you what you typed in for privacy reasons. Once you have successfully able to remotely connect to a computer located in cse basement.
3. **Trying Some Commands**
No we will run some commands, as you may know there are several commans that can be used in a terminal, commands including, but not limited too,  cd~, cd, ls -lat, ls -a. Once in the server you may want to sign out and go back to your own computer you can enter CTRl -D and then enter the command *exit*. These are just a few commands that you can use to try **running some commands**. 

4. **Moving Files with *scp*:** 
Now we will learn how to move file by using scp. To clarify we will be using the scp files on our server thus you should make sure you ran the previos step of how to exit eing6. To define what in fact is scp, scp is a.. In order to move a file we must create the file called aaa.java where you can input any word for aaa. After creating the new file and put whatever code you desire within it. After creating the file on your terminal you can enter, scp **aaa.java cs15lsp22mm@ieng6.ucsd.edu**. You will then be promoted to enter your password. Next you will again login to your course specific account ieng6 aso you can follow step 
2 remotely connecting. Now you will types ls and press enter to notice that its in your home directory. Thus we have been able to succesfully **move the file using scp**
5. **Setting an SSH key:**
Now we will set an SSH Key. To set this SSH key we will frist make sure you are in your computer thus do not have your ieng. If you are not in your computer then follow steps in 3 to exit. Then you will enter ssh-keygen. Next you will enter the file that which you want your key to be saved in, by entering (/Users/<user-name>/.ssh/id_rsa): /Users/<user-name>/.ssh/id_rsa
After this has been inputed you will asked to enter a passphrase that which you do not have to so just press enter again. After pressing enter twice you would have been able to successfully saved your identification and public key. Now to get out public key to our .ssh directory we can copy our public key to the ssh. directory on server. Enter ssh cs15lsp22mm@ieng6.ucsd.edu
then enter your password which like similar to step three we have just logged onto cse computer basement. Now to exit and go back to your computer you will enter mkdir .ssh . Now to save your username and passwrod you will enter scp /Users/<user-name>/.ssh/id_rsa.pub cs15lsp22mm@ieng6.ucsd.edu:~/.ssh/authorized__keys. In order to check if we did it correctly we can by using ssh again to login like from step 3. 

6. **Optimizing Remote Running**
Now we will teach you how to optimize remote running. This is done by first


**CSE 15L Spring 2022 Announcement**
Have a  _nice_  week!
We will be using [Autograder](https://autograder.ucsd.edu) as the student queue during TA/tutor office hours.
[Link][1]
⋮
[1]: http://b.org

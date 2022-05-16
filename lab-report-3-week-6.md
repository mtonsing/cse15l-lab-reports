# Lab Report 3:implementing option 1-3 from *lab 5*
Now we will be implementing options 1-3 from lab five which include, streamlining ssh configuration, Setup github access from ieng6 and copying whole directories with scp -r.

## Streamlining ssh Configuartion
We will now show you how to log into your 
ieng6 account without having to insert 
your own password.
* We will first do so by typing in the terminal
`~/.ssh/config` and if you cannot open it becuase it doesn't exist you
will need to create it.
* Then on your file call config you must paste
the following lines onto the file, see the second  screenshot to see the format that which it should be indented.
* **Host ieng6 
    HostName ieng6.ucsd.edu
    User cs15lsp22zz (replace cs15lsp22zz with your own username)**
* In order to edit the file you must type on the terminal `vim config` which will then make the terminal look like the image below, where you can now edit it. In my case I changed my alias to be now Maria. Once you have paste the lines above and finish editing the file to escape you will need to enter `esc` and then type `:wq` and press enter. This will then save the changes made into config. 
* Here is an image of how I was able to open config and edited my file config.

![Image](photothatgetserror.png)

* Below is an image of editing the config and choosing my alias to be Maria, as it was ieng6 before.
![Image](Labreport3image2.png)
* Now once you have edit the file you should now be able to
type in the terminal `ssh ieng6` or if you have chosan another alias like me I will need to type `ssh Maria`.
* Here is an image of how it will look like if everything is
implemented correctly. 
![Image](labreport3image3.png)
* Next we will show an **scp command copying a file to our account using the alias we have chosen** which for me will be Maria. So first make to sure exit your ieng6 account. Since we have now streamline our ssh configuartion we only need now to type,
`scp practice.java Maria:~/` (replace practice.java with file you want to copy and Maria with the Alias you have chosen) such that if we want to make sure we have copy the file to our account we can enter `ssh Maria` to log back into our account then `ls` which shows a list of files in the current directory where we will then see our file in this
case practice.java was succesffuly copied over to our account.
* Below is an image demonstrating this
![Image](Labreport3image4.png)


## Setup GitHub Access from ieng6
Now we will show you how setup GitHub access
from ieng6
* We can see that if we make a edit on our file this case Markdownparse.java such as trying to 
do add,commit,push the do enter `git status` we will get an error because we need to be able to use a token-based mechanism such as ssh. To fix this issue we will create both a public and private key. 
* One can create a public by going to [github](https://github.com/), then going to **settings**, then then **ssh and GPG keys** where I made my public, **report3key**.
* Below is an image of my public key located in github.
![Image](keysss.png)
* Likewise I created a private key. Below is an image of how I created my private and public key and where it is stored in my account. I first logged onto my account my entering `ssh Maria`. To create this key I enter `ssh-keygen` and then press enter three times until we are given the keys random art image. We can see on the last line after entering `ls` that id_rsa is my **private key** and id_rsa.pub my **public key** location.
* Below is an image of the location of both my public and private key.
![Image](progress.png)
* Below is an image a part of my public key.
![Image](actualprivateKey.png)
* Once we have our private key and public key created we will now **make change to our markdownparse file and push to GitHub from our ieng6 account**. Below is an image of me running git commands to commit and push a change to Github while being logged into my ieng6 account. For instance I change the current directory to markdown-parser.And the edit I make is creating a new file a.md. I create this file by entering `touch a.md` then I enter the git commands, first `git add .` to add new edit then `git commit -m "new file"` , to explain what was the edit and to commit this edit and then I am able to push by entering `git push` . As image below shows we are successfully able to do this. 
![Image](labreport3part2.png)
* As we can see we get no errors this time.
* Here is a link to for the resulting commit, that I was able to attain by going to my person account on github then going to my respository for markdown-parser and selecting the edit **new file** to get the link,
[Link to resulting commit](https://github.com/mtonsing/markdown-parser/commit/291862536fd07157aa4782a13a47b3b42fd0c661)
## Copy whole directories with scp -r
Now we will show you how to copy whole directories with scp -r meaning copying the directory and all files that fall within a directory and further on. 
* In order to copy a certain directory you must type into your
terminal `scp -r . cs15lsp22@ieng6.ucsd.edu:~/markdown-parse`. Where in this case we are copying the
directory markdown-parse onto the remote server if it
had not already existed as well copying all of what can 
be found of this given directory. Thus once this has been 
called we can log into the server and be able to see all of our files there in the specified directory which in this case is 
markdown-parse. 
* Below is an image of succesfully copying whole markdown-parse directory to specific ieng6 account.
![Image](image17.png)
![Image](image20.png)
* Now since we have copied the whole markdown-parse directory to my ieng6 account we can now try running the test that are found within this directory, thus we should be able to run the test in our ieng6 account by typing the command, 
`javac -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar MarkdownParseTest.java` to first compile the MarkdownParseTest.java and then after typing the command `java -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore MarkdownParseTest` to run MarkdownParseTest.java.
* Below is an image of logging into my ieng6 account then compiling and running the test for my respository.
![Image](screenshotoftest.png)
* Now lastly we will demonstrate how to combine **scp, ; and ssh** to copy whole directory and run the test in one line. This can be done by combining these commands which are copying whole directory,logging into one's ieng6 account and lastly running the test, by entering in on the terminal, `scp -r . Maria:~/markdown-parser; ssh Maria "cd markdown-parser; /software/CSE/oracle-java-17/jdk-17.0.1/bin/javac -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar MarkdownParseTest.java; /software/CSE/oracle-java-17/jdk-17.0.1/bin/java -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore MarkdownParseTest"` all in one line. The first part before the semi-colon is coppying the whole markdown-parser to my ieng6 account the secont semi-colon is to log onto my ieng6 account and the last two semi-colons are to compile and run the test. 
* Below is an image of doing this. To not show again copying the entire directory as image before here is a simiplify versions showing I was able to copy and run the test succesfully. 
![Image](copyingtest1.png)








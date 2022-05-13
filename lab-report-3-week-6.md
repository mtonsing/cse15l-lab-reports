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
the following lines onto the file
* **Host ieng6 
    HostName ieng6.ucsd.edu
    User cs15lsp22zz (replace cs15lsp22zz with your own username)**
* In order to edit the file you must type on the terminal `vim config` which will then make the terminal look like the image below, where you can now edit it. In my case I changed my host to be now Maria. Once you have paste the lines above and finish editing the file to escape you will need to enter `esc` and then enter `:wq`. This will then save the changes made into config. 
* Here is an image of how I edited my file config.
![Image](Labreport3image2.png)
* Here is an image of opening my config file and
editing it so that my host name is now instead Maria instead of ieng6.
* Now once you have edit the file you should now be able to
type in the terminal `ssh ieng6` or if you have change your host name like me I will need to type `ssh Maria`.
* Here is an image of how it will look like if everything is
implemented correctly. 
![Image](labreport3image3.png)
* Next we will show an scp copying a file to our account using the alias we have chosen which for me will be Maria. So first make to sure exit your ieng6 account. Since we have now streamline our ssh configuartion we only need now to type,
`scp aaa.java Maria:~/` (replace aaa.java with file you want to copy) such that if we want to make sure we have copy to our account we can enter `ssh Maria` to log back into our account then `ls` which we will then see our file in this
case aaa.java was succesffuly copied over to our account.

## Setup GitHub Access from ieng6
*first we will add a public key, this can be done by following
this [link](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)

## Copy whole directories with scp -r
Now we will show you how to copy meaning copying the directory and all files that fall within a directory and further on. 
* to simply copy a certain directory you must type into your
remote server `scp -r . cs15lsp22@ieng6.ucsd.edu:~/markdown-parse`. Thus in this case we are copying the
directory markdown-parse onto the remote server if it
had not already existed as well copying all of what can 
be found of this given directory. Thus once this has been 
done we can log into the server and be able to see all of our files there in the specified directory which in this case is 
markdown-parse. 
* here is an image of succesfully copying whole markdown-parse directory to specific ieng6 account.
![Image](image17.png)
![Image](image20.png)




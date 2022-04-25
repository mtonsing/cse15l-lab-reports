# Lab Report 1:How to fix a bug
Now we will show you to fix bugs when the output is 
not what you desire. 
In the code we will be using our goal is to be given a file's name and the link name and be able to print only the link and not the file name. While the accurate way to print a link is by putting the name of the link you want to show in brackets and have the following be parenthesis with the link it's possible for a user to input the wrong code.

## When we have several blank lines after the file names.
* The image below shows a screenshot of the code change diff from Github that help
fix the bug that is produce when one input to file names as well as several blank lines after. Which was inserting an if statement.
![Image](image1.png)
* Here is a link to the test file that that made me prompt change in my code. This 
error was that it had several blank lines after inputing the links.
[test file](https://github.com/mtonsing/markdown-parser/blob/main/test-file.md)
* To show the symptom of the failure inducing input here is an image of the output of running the file with this specific error case.
![Image](erorrforseverallines.png)

*  The bug of this error is that the while loop within my code keeps going becuase
it believes that there is going to be another link to add to the string which is inaccurate. Thus is why we get see from our symptoms of outofmemory when we have our failure inducing input which was the several blank lines after the code we care about which is the links. 
## Trying a file that uses [] and not () .
* Here is an image showing a screenshot of the code change diff from Github which as can be seen I fix it by using a if statement to first check if there is any "(" within the code.
![Image](newimage3.png)
* Here is a link to the test file that cause me to make a change in my code.
[test file](https://github.com/mtonsing/markdown-parser/blob/main/test2-file.md)
* The image below shows the symptom of the failure inducing input which was a file that uses brackets and not parenthesis. 
![Image](Error2.png)
* We can see the bug was that in the code we relied that there was always going to be both a parenthesis and brackets but this is untrue for the given test file. Thus is how we attain our symptom which is getting a return statement but it being incorrect for the return statement we actually wanted to produce. The failure inducing input was the root of the problem so now fixing this case we can test other files that also only contains parenthesis and no brackets and making sure to return the second () as the first typically is the name of the file and not the link. 
## A file that uses () and not [].
* Below is an image of how I was able to fix this symptom which was by including an if statment to check if there is any "[" within the code. 
![Image](fixederror3.png)
* Here is a link to the test file that contains the failure inducing input and made me prompt the change above.
[test file](https://github.com/mtonsing/markdown-parser/blob/main/test3-file.md)
* This is the output for when our file only use parenthesis and no brackets.
![Image](error3.png)
* Likewise with our other problem we see that the the user only inputs parenthesis and no brackets so we are getting the wrong output which is our symptom, and the bug is that our code just prints and stops at the first set of parenthesis as it is unable to find more brackets. With the failure inducing input we acknowledge that we must also make sure that when the user only uses parenthesis and not brackets that we are still printing only the links and not the file's name. 


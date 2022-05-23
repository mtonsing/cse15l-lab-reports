# Lab Report 4:*Testing three snippets* on my own markdown-parse and on the markdown-parse I reviewed on lab 7
## Testing 
* In order to test all my new test I inputed into
my terminal `javac -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar MarkdownParseTest.java` and after pressing enter I type in the terminal, 
`java -cp .:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar org.junit.runner.JUnitCore MarkdownParseTest`
## Link to markdown-repository
* Here is a link to my own markdown-parse repository, [Link](https://github.com/mtonsing/markdown-parser)
* Here is a link to the markdown-parse repository that I reviewed, [Link](https://github.com/thanhnhanlam/markdown-parser) 
## Test Snippet One
* Testing snippet One on markdown-parse I reviewed on lab 7. Below is a photo of first of how I created the test in my markdown parse test file. The second image is the file componenets. And lastly the last image shows if it fails or pass as it can be seen our test failed in this case. The following test snippets follow same procedure.
![Image](photopart1.png)
* Testing snippet One on my own markdown-parse.
Below is image of testing snippet one to my own markdown-parse file. I do not included image of what the file we are testing contains becuase its identical to the image that was previously shown. As is seen our test fails. 
![Image](a.png)
* After testing I feel that there will need to be a code change in order to fix the error a code that is less than 10 lines will be do able I feel.The code change for this specific test I feel would be, not letting back ticks effect the lines of code that which we want to run since we see from the results our code stops after the second back tick thinking that our code is done. 
## Test Snippet Two
Testing snippet two on markdown-parse I reviewed on lab 7. Similary follow same procedure to now test snippet two as it can be seen our test fails. 
![Image](photopart2.png)
* Testing snippet two on my own markdown-parse.The image below shows how I created the test in my markdown-parser test file and what part my test fails as it can be seen this test fails as well.
![Image](b.png)
* After testing I feel that there will need to be a code change in order to fix the error a code that is less than 10 lines will be do able I feel. This specific code that will fix this error I feel will be to be sure to print only characters that a webiste can contains such as letters numbers back slashes making sure to not print the parenthesis ever, will help us get our desired results. 
## Test Snippet Three
Testing snippet three on markdown-parse I reviewed on lab 7.Below is an image of how i was able to test snippet three on the markdown parse that i reviewed in lab 7. As we can see the test fails. 
![Image](photopart3.png)
* Testing snippet three on my own markdown-parse.
Similar process to the past steps we see that our test fails after recreated my test in my parsetest-file in order to save gas. 
![Image](c.png)
* After testing I feel that there will need to be a code change in order to fix the error a code that is more than 10 lines. The specific code that would fix this error I feel will be a take longer lines to see which index to print such that removing the unnecessary spaces from our print statements so that our links are all seperate by only a comma and not multiples spaces. 
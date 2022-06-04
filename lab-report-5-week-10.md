# Lab Report 5:Using two test where my implementation had different answers than the implementation provided in *lab 9*
## How I was able to find the test with different results
* By implementing what was done in Lab 9, I was able to find the test
with different results. I did this through the process of using vimdiff on the results of running a bash for loop.And then scrolling through to see which test contains different results.To specify with more details I first I created two result.txt which contains the output of each test file as done in lab 9. By first editing the provided file, scipt.sh that is provided to also print out the name of each file before it's output by adding the line `echo "$file"`. I was able to create result.txt by typing the following in the command line, `bash script.sh > results.txt`, which will save all output of each file to one file, results.txt. I then followed the same steps to get a results.txt for my own markdown-parse. Once I had two results.txt files I then opend it using vimdriff by typing the following command, `vimdiff markdown-parser/results.txt cse15lsp22-markdown-parser/results.txt` which led me to the following image below. Here the left side demonstrate my for a specific test file output for my own markdown-parse and the right side demonstrate the output for the same test file of the given markdown-file provided in lab 9. I can then scroll to I see a pruple line which means the output for the same test file is differs between mine and the markdown-parser provided in lab 9.And to exit this screen I do so by using escape + "`:q`" twice.
![Image](fulltestfiles.png)

## Link to test files with different results
* Link to test file 194
[Link to test file 194](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/194.md)
* Link to test file 201
[Link to test file 201](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/201.md)
## Test File 194
* Below is an image of the actual test file
![Image](insidefile194.png)

* Which implementation is correct: By using [commonmark](https://spec.commonmark.org/dingus/) I was able to see that the correct implementation was neither since the expected output was *title (with parens)*. Since we can see my actual output was an error messages which showed that there is no valid link while the the markdownparser provided in lab 9 was *[url]* which is also wrong. 
* Both actual outputs and expected output:
As was mention previously we see that the expected and actual output are not at all the same here is the image of actual output for test file 194 for mine and their implementation. 
![Image](actual1941.png)

* The bug/The code that should be fix: Since both cases are wrong
since neither is printing the correct output we will choose my code to fix. In my case my code think there is not valid link which is not the case thus one of our cases where we check if the link is a valid link is incorrect. Since in my output I get that it’s not a valid link with the same error message in the image below it will be helpful to first make sure this code is changed such that we get that this is a valid link and so we can get the right output. In my code I try to first find the index of the openParen from the  index of close parenthesis and thus if not found openParen will equal -1 while the first iteration works we get a set of brackets then a set of parenthesis but the next time we have brackets occurs at the end of our given test file 194 thus when looking for the first occurrence of open paren after the second closeBracket we get an error since there does not exist an open Parenthesis after the second set of brackets. Therefore to fix this code we will need to make sure since we have a while loop which i still think is is needed we should not print the error message if we were able to successfully add a link, URL thus I feel we need to add this link and on our next while loop when we get this open Parenthesis error we will exit the loop but still print out the link found and we will not have an error since we were able to successfully print out at least one link. 
![Image](codefix.png)
## Test File 201
* Below is an image of the actual test file 
![Image](inside201.png)
* Which implementation is correct:
For this test file it's clear that the correct implementation is, my implementation of markdown-parser, where the actual output and the expected output for test file 201 is,an empty list since no link is valid.In this case the given implementation in lab output was incorrect since its output was, *[baz]*.
* Both actual outputs and expected output:
As mention before we see that my actual output is similar to the expected output, while the give implementation of lab 9 output is incorrect. Below is an image of the actual output for both implementation.
![Image](actaulresult2.png)
* The bug/The code that should be fix:
In this case mine has the necessary output since no link should be printed out since the code in test file 201 is invalid. As we can see in my case we again get an Open parenthesis error. Thus since mine is correct we will look into the markdown parser given to us to see where a code fix is possible to fix this error since their test file is printing out a link which is, baz. From the code in test file 201 I can see the error is that there are characters in between the bracket and parenthesis when in reality we should have brackets followed by parenthesis. Thus looking into their markdown parser we can see that a while loop could be what is causing this problem since in the lines of code demonstrated below function is to get first set of brackets then first pair of parentheses without consideration that there can be something in the middle, and if there is should be an error. This is why in this implementation we are still outputting a link, [url]. 
![Image](actualresult2.png)

# Lab Report 5:Using two test where my implementation had different answers than the implementation provided in *lab 9*
## How I was able to find the test with different results
* By implementing what was done in Lab 9, I was able to find the test
with different results. I did this through the process of using vimdiff on the results of running a bash for loop.And then scrolling through to see which test contains different results.To specify with more details I first I created two result.txt which contains the output of each test file as done in lab 9. By first editing the provided file, scipt.sh that is provided to also print out the name of each file before it's output by adding the line `echo "$file"`. I was able to create result.txt by typing the following in the command line, `bash script.sh > results.txt`, which will save all output of each file to one file, results.txt. I then followed the same steps to get a results.txt for my own markdown-parse. Once I had two results.txt files I then opend it using vimdriff by typing the following command, `vimdiff markdown-parser/results.txt cse15lsp22-markdown-parser/results.txt` which led me to the following image below. Here the left side demonstrate my for a specific test file output for my own markdown-parse and the right side demonstrate the output for the same test file of the given markdown-file provided in lab 9. I can then scroll to I see a pruple line which means the output for the same test file is differs between mine and the markdown-parser provided in lab 9.And to exit this screen I do so by using escape + "`:q`" twice.

## Link to test files with different results
* Link to test file 194
[Link to test file 194](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/194.html.test)
* Link to test file 201
[Link to test file 201](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/201.md)
## Test File 194
* Which implementation is correct:
* Both actual outputs and expected output:
* The bug/The code that should be fix:
## Test File 201
* Which implementation is correct:
* Both actual outputs and expected output:
* The bug/The code that should be fix:
# Lab Report 5

To find the testfiles with different resuts, I directed the output of the scripy.sh to a file using ```bash script.sh > results.txt```. Using ```vimdiff```, I compared the result.txt files of the given markdown-parser repository and my markdown-parser repository. Then, I picked at random some files that resulted in differences, and looked at the original file to see what it contains. This way, I could see why there may have been differences based on the MarkdownParse code. 

## Test 1
- [516.md](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/516.md) <br>
- The given repository was not correct, but mine was. When we were first developing MarkdownParse.java, we had to take into consideration images, which are very similar in format to links. To combat this, I implemented code that checked for an exclamation point before the openBracket, therefore sorting images from links. The given repository did not do this.
- outputs: mine and the given respectively <br> 
![Image](516-outputs.jpg) <br>
- expected output: according to the CommonMark demo site <br>
![Image](516-expected.jpg) <br>
- for one incorrect implementation, screenshot + highlight code that needs to be changed ++ describe the bug 

## Test 2
- [521.md]

my repo wrong, i said that it had to end in like .html or smthn to be valid- should remove that line
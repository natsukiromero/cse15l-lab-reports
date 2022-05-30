# Lab Report 4
testing MarkdownParse with various snippets <br>

## Repositories
[my repository](https://github.com/natsukiromero/markdown-parser) <br>
[other repository](https://github.com/tcarman/markdown-parser) <br>

## Snippet 1
Test written: <br>
![Image](1-1.jpg) <br>

Test Results in My Repo: <br>
![Image](2-1.jpg) <br>

Test Results in Other Repo: <br>
![Image](3-1.jpg) <br>

Corrections: I think that this case would be fixable. For the "url.com," I would add code that checks the inline code for backticks and, if present, removes them. This way, you could continue through the code with a substring with the proper formatting to return the url. As for ucsd.edu, I may be able to adjust the code so that int closeBracket is the latter ]. My current code says that if ] and ( are not back to back, it is not a valid link, so by changing what the code views as ] would fix the problem. In other words, make sure to account for nested brackets. (Note: I have not thoroughly thought through the implications of whether or not this would mess up other test cases.)

## Snippet 2
Test written: <br>
![Image](1-2.jpg) <br>

Test Results in My Repo: <br>
![Image](2-2.jpg) <br>

Test Results in Other Repo: <br>
![Image](3-2.jpg) <br>

Corrections: Fixing my code for this snippet would be the same as proposed for snippet1- adjust the indexes used so that the last ) or ] (as considered by VSCode preview) is used. In order to do this, I would have to consider the whole line as a substring, and then search for all the brackets and parenthesis. I would then have to compare the indices of multiples to each other to ensure that I am using the right ones, then return whatever index I decide upon to the ints to be used to get the url. This way, the full a.com(()) would be printed, and example.com would not be ommitted.

## Snippet 3
Test written: <br>
![Image](1-3.jpg) <br>

Test Results in My Repo: <br>
![Image](2-3.jpg) <br>

Test Results in Other Repo: <br>
![Image](3-3.jpg) <br>

Corrections: Due to what I personally had considered a "valid link," any link with spaces in it was considered invalid. In order to return both twitter.com and cse.ucsd.edu, I would simply need to remove the few lines that filter those types of links out. AS far as returning https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule, I already have code that removes spaces from the links. In order to return this link, I would want to write similar code that removes line brea]ks/'enter's from the link, perhaps by making sure the url substring begins and ends at the an actual letter/number.
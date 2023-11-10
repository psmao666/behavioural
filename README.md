# My behavioural question answers

# Table of contents
1. [What was the most difficult bug you have encoutered and how did you fix it?](#problem_solving_1)
2. [Tell me about a time you found a creative solution to a problem?](#problem_solving_2)

## Problem Solving

### What was the most difficult bug you have encountered and how did you fix it? <a name="problem_solving_1"></a>

#### Situation
In my previous project of the web crawler, I was working on a new feature that was designed to improve the crawling speed.
During testing, I found that under certain circumstances, the new feature was causing the application to crash, which was
a major issue as it would disable the whole program.
#### Task
My task was to identify the root cause of the crash and to refactor the code in order to apply the new feature to the program 
without any potential bugs.
#### Action
I started by conducting a thorough review of the code to see if I could identify any obvious issues, but that didn't yield any
results, so I decided to run a series of testing on extreme cases. After carefully reading the logs and benchmark measuring, 
I noticed that the crawler crashes only when there are enourmous number of users. I then did researches online to see if there 
is any similar bug, and communicated with my friends who have more industrial experience than me, turns out the bug was the 
result of memory leak. I watched editorials online about smart pointer (which is a new technique introduced in C++11), and 
spent several hours on refactoring the code with smart pointer.  
#### Result
After completing the refactor, I ran the code again and it worked properly at the same circumstance, and I tested it several more rounds to 
ensure the bug is fixed and no additional bug was introduced after the fix. 
#### Reflection
This experience taught me a lot about the importance of thorough and methodical testing and debugging, and how crucial it is to 
keep up-to-date with modern technology.

---

### Tell me about a time you found a creative solution to a problem? <a name="problem_solving_2"></a>

#### Situation
It was an open problem on Australian Informatics Olympiad website, the problem basically asked you to construct a way to connect nodes in 
a graph in order to minimise the cost which is calculated in a special way. This problem had a ranking system where people are sorted by 
how approximate their solutions are.
#### Task
Achieving an above-average mark was trivial, but I am a person who feels very uncomfortable if someone can achieve a perfect score and I can't.
Therefore, I spent over 2 months on trying to optimise my algorithm.
#### Action
I started by going through the details in the problem description again, and wrote a bruteforce solution which gave the right answer but was too slow to meet 
the time constraint, I used it to generate the right output of a large amount of data, in order to set up for the testing of my solution. It turns out 
that my solution could degrade to a very slow algorithm if the input graph forms a chain. After carefully analysing all the possible data, I realized this is
the only issue. I then came up with the randomization algorithm to optimise my solution, and to mitigate the possible risks of not getting an accurate answer,
I tested the new solution against around 10000 test cases and all of them worked properly.
#### Result
After submitting this solution to the website, I scored 99.8/100 and came first on the leader board. It was my first time using randomisation algorithm to solve 
problem.
#### Reflection
This experience taught me a great deal about the value of thinking outside the box and the importance of examining the risks and potential bugs while introducing 
new approach.

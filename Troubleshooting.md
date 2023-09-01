* See -help- in Stata to ensure that you have the correct syntax. Advice from chatGPT: "Debugging can be frustrating, but it's important to stay calm and positive. Approach the problem with a positive attitude and a belief that you can solve it." See [more debugging tips](https://github.com/aadityadar/all-aboard/wiki/Troubleshooting#debugging) below.

## Asking questions:

* Asking good questions is not easy and takes practice. Be clear, specific and concise. A decent format is:  
  - I am trying to do XX  
  - I tried XX and got the error XX (mention all relevant attempts)  
  - Screenshot attached/code and error pasted below  

* [Statalist](https://www.statalist.org/forums/help#sources) offers great advice on how to ask questions. 

> 9. Where may I look for other advice on posting technical questions?
> 
> You might find various websites that discuss general issues in getting help from technical lists and forums instructive and even amusing. Mike Ash discusses “Getting answers” at http://www.mikeash.com/getting_answers.html, with key headings:
> 
>     Explain what doesn’t work
>     Provide everything up-front
>     Post your code
>     Do your research beforehand
>     Do your research during
>     Do your research afterwards
>     Don’t post the same question repeatedly
>     Follow up after you get an answer
>     Treat the list like people
>     Always consider the answer
> 
> Eric Raymond and Rick Moen discuss “How to ask questions the smart way” at http://www.catb.org/~esr/faqs/smart-questions.html.
> 
> Asking about your real problem, not something else, may seem too obvious to mention, but do check http://xyproblem.info/.
> 
> 10. How should I write questions?
> 
> Do write carefully; be precise and include all relevant detail.
> 
> For instance,
> 
>     Don't say "Stata crashed" when you mean "Stata issued an error message" (and then tell us the error message). Say crashed only if you mean crashed as in crashed and burned.
>     Don't say "many variables", say "around 50 variables" or, even better, "52 variables".
>     Don't say "a big dataset", say "a dataset of 50 variables and approximately a million observations".
>     Don't say "I ran a regression and then ...", say "I ran regress and then ...". 
> 
> Please pay attention to grammar, spelling, punctuation, and tidy, readable presentation generally. Statalist is naturally sympathetic whenever it is clear that English is not your first language (which is another reason to use your real name). 

* [How To Ask Questions The Smart Way by Eric Steven Raymond](http://www.catb.org/~esr/faqs/smart-questions.html)

> Use meaningful, specific subject headers  
> Make it easy to reply  
> Write in clear, grammatical, correctly-spelled language  
> Send questions in accessible, standard formats  
> Be precise and informative about your problem  
> Volume is not precision  
> Don't rush to claim that you have found a bug  
> Grovelling is not a substitute for doing your homework  
> Describe the problem's symptoms, not your guesses  
> Describe your problem's symptoms in chronological order  
> Describe the goal, not the step  
> Don't ask people to reply by private e-mail  
> Be explicit about your question  

* [XY problem](https://xyproblem.info/)

> The XY problem is asking about your attempted solution rather than your actual problem. This leads to enormous amounts of wasted time and energy, both on the part of people asking for help, and on the part of those providing help.
> 
>     User wants to do X.
>     User doesn't know how to do X, but thinks they can fumble their way to a solution if they can just manage to do Y.
>     User doesn't know how to do Y either.
>     User asks for help with Y.
>     Others try to help user with Y, but are confused because Y seems like a strange problem to want to solve.
>     After much interaction and wasted time, it finally becomes clear that the user really wants help with X, and that Y wasn't even a suitable solution for X.

* [Strunk's Elements of Style: Elementary Principles of Composition](https://www.bartleby.com/lit-hub/the-elements-of-style/)

>    Make the paragraph the unit of composition: one paragraph to each topic  
>    As a rule, begin each paragraph with a topic sentence; end it in conformity with the beginning  
>    Use the active voice  
>    Put statements in positive form  
>    Omit needless words  
>    Avoid a succession of loose sentences  
>    Express co-ordinate ideas in similar form  
>    Keep related words together  
>    In summaries, keep to one tense  
>    Place the emphatic words of a sentence at the end  

* [Writing the perfect question](https://codeblog.jonskeet.uk/2010/08/29/writing-the-perfect-question/) by Jon Skeet 

## Debugging

Tips for debugging (via chatGPT)

1. **Understand the Problem**: Make sure you completely understand the problem. What is the error message? What part of the code is it referring to? What is supposed to happen, and what is actually happening?

2. **Reproduce the Error**: Make sure you can consistently reproduce the error. If the error is sporadic and can't be consistently reproduced, it will be very difficult to debug.

3. **Read the Error Message**: Stata's error messages often contain valuable information about what went wrong. Make sure to read it carefully.

4. **Isolate the Problem**: Try to isolate the problem to the smallest amount of code possible. This often involves commenting out sections of code until the error no longer occurs.

5. **Check Data Types and Structures**: Ensure that the data types and structures are what you expect them to be. Some Stata commands require the data to be in a certain format or structure.

6. **Check for Missing Values**: Missing values can often cause unexpected behavior or errors in your code. Make sure to handle these appropriately.

7. **Check Variable Names**: Ensure that you are using the correct variable names. Stata is case-sensitive, so be careful with capitalization.

8. **Use Built-in Debugging Tools**: Stata has a `trace` command that allows you to see each command as it is executed. This can be very helpful for tracking down the source of an error.

9. **Check for Common Mistakes**: There are certain common mistakes that programmers often make in Stata. For example, accidentally using `=` instead of `==` in a conditional statement, or not properly specifying the options of a command.

10. **Get a Fresh Pair of Eyes**: Sometimes you can be staring at a piece of code for so long that you can't see the obvious mistake. Ask someone else to take a look at your code. They might spot something that you missed.

11. **Take a Break**: If you've been working on a problem for a long time and can't seem to make any progress, take a break. Sometimes stepping away from the problem for a little while can give you a fresh perspective.

Remember, debugging is a skill that takes practice. The more you do it, the better you'll get at it.
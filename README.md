* TOC
{:toc}

# Overview
## Background
I've interviewed at dozens of companies over my career. As an interviewee, I've found that practicing the following structured format helps me succeed more consistently at tackling technical interviews at large tech companies. I've also shared this with many others who have found it useful as well.

I've also interviewed over 50 candidates in my professional career, mostly at Google but with some at Microsoft and a startup. As an interviewer, I'm often looking for a positive *signal* that a candidate has certain qualities, such as strong communication skills, problem solving, programming, and testing. I've found that candidates who approach interviews using a structured format have a much easier way showing positive signals than those who don't.

## Setting
This process is tailored for 45-minute tech interviews where most of the interview time is spent on one design or programming problem, potentially with follow-ups. You may need to use a shorter version of this process (or omit certain parts) if your interview is shorter, or if you're expecting several short, unrelated questions.

## Goals
The goal of a technical interview is to convince your interviewer that you have certain qualities they're looking for. The goal is *not* simply to show that you can find an optimal solution to some esoteric problem. The biggest artefact of your interview is the impression that your interviewer has about your communication, problem-solving approach and ability to write code. Even if you have those qualities, they won't do much good if you can't show them during the interview, so it pays to invest in a good process that showcases these skills and gives you the best chance at success.

# Process
Once you're given an initial problem statement, the process is as follows:

## 1. Understand the problem
*[Timebox to ~5-10min]*

Interviewers will often give a vague initial problem statement to see how well the candidate deals with ambiguity and verifies their assumptions. This is your opportunity to make sure you have a good grasp of the problem before you dive deep into solutions.

**Do**:
- Identify the critical parts of the problem.
- Ask clarifying questions.
- State any assumptions you have.

**Don't**:
- Jump to solutions.
- Make hidden assumptions.
- Over-focus on edge cases (this is even more important for design problems).

## 2. List test cases
*[Timebox to ~5min]*

Coming up with test cases early is the best way to ensure you've done the [previous step](#1-understand-the-problem) correctly. Specifically, good test cases will help you identify the most difficult parts of the problem, give you a clear contract to design for, and show good initiative and critical thinking. The last thing you want is to start testing after you've implemented something and realize you've solved the wrong problem.

**Do**:
- Add test cases for the common use-case and a handful of important edge cases.
- Describe the test cases as a clear contract, ideally with a table of inputs --> expected outputs (or behaviors).

**Don't**:
- Be vague or hand-wavy about your tests (e.g. describing inputs without expected outputs).

## 3. Explore multiple design ideas
*[Timebox to 10 min]*

It's rare that somebody would come up with an optimal solution to a problem from the start. Usually, it's better to brainstorm a few possible solutions (including a "naive" solution) before committing the rest of your time to implementing a specific one. Besides, once you have a few high-level solutions down, it's easier to compare apples-to-apples.

**Do**:
- Try to explore at least 2 different solutions to the problem.
- Flesh out just enough of each solution to get a sense for the high-level steps and big-O notation of its runtime and space complexity.
- Get a quick ACK from your interviewer before committing to a solution.

**Don't**:
- Immediately discount the "naive" solution. Not only does it serve as a useful baseline to compare to, but when compared with other options, it can actually end up being the best solution according to some criteria (e.g. simplicity or memory) and not that much worse in others (e.g. runtime).
- Spend too much time exploring esoteric variations. Once you have 2 or 3 solid approaches, consider picking one and moving on.
- Get too deep in the weeds of any particular solution, unless the details are relevant for the big-O notation.

## 4. Implement one solution
*[Timebox to 15-20 min]*

Once you find a promising high-level solution, try to divide the problem into smaller blocks and implement those. If your code will be large or complex, it may be helpful to start by writing your solution in pseudo-code, then turn it into an outer function that calls other smaller functions which each implement a smaller piece of the solution. If your code is small enough to be implemented in one function, then just do what makes sense :-)

**Do**:
- Divide large or complex functions into smaller ones with clean abstractions.
- Try to use clear variable names that are easy to understand.
- If you forget a library function signature, either ask your interviewer or just make up a reasonable signature and write it on the side.

**Don't**:
- Spend too much time over-optimizing unnecessary details.

    Get most of your solution working first before you start optimizing small things.

## 5. Test your code
*[Timebox to ~10 min]*

Once you've implemented your solution, take the time to look for any obvious bugs or mistakes, then start to run through the test cases you've written down from step #1. Be detail-oriented with at least your first test case, and avoid skimming large parts whose answer you think you know.

**Do**:
- Keep track of variables and their values over time. Consider adding comments at the end of the line with the variable's current value, or a table with each variable's value over time.
- Be detail-oriented while executing the code.
- Take special note of edge cases (e.g. the first or last iteration of a loop).

**Don't**:
- Skip some parts of the code that you haven't run through previously.

    If there's a bug you missed there, this shows as a lack of attention to detail.

# Common pitfalls
## Not utilizing your interviewer
A good interviewer is not out to get you, but wants to accurately record your best performance. In my experience as an interviewer, most people don't utilize the interviewer enough, and as a result they miss opportunities for help (at best), or give off the vibe that you're defensive.

**Do**:
- Ask for a hint if you're stuck.

    If you do, make sure to clarify your thought process until that point, the ways you can go from there, and why you don't think any of them would work.

- Clearly communicate your assumptions.
- Talk through your thought process as you go.
- Follow your interviewer's lead where it differs from the steps above.

    For example, your interviewer might want you to split your time over implementing multiple solutions.

**Don't**:
- Be lazy.

    It's okay to use your interviewer as a sounding board and get their thoughts every now and then, but make sure you're still showing critical thinking and coming up with independent solutions.

- Stay quiet for more than 2-3 minutes.

    Even if you need quiet time to think, make sure to give periodic updates to your interview on what's going on in your mind.

## Losing track of time
Most candidates I've interviewed probably would have solved the problem given enough time. The challenge is that they don't have unlimited time -- part of what you're showing in an interview is that you have an efficient process to solve problems. Some companies (e.g. Google) even have an explicit rubric for efficacy with regard to time.

It's almost always better to complete a solution that's mostly good but could use small improvements, rather than perfecting some small or unimportant parts while leaving critical pieces of the problem unsolved.

**Do**:
- Timebox various parts of the process above (see recommendations).
- Prefer incremental progress to perfection.
- Consider wearing a wrist-watch to the interview.

**Don't**:
- Panic if you're behind schedule.

    Instead, work with your interviewer to prioritize the most important parts of the problem and skip others.

- Entertain black-or-white thinking (e.g. "if I don't get the optimal solution I won't get an offer").

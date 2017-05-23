---
layout: post
title:  Lessons learned in my first month
date:   2017-05-23 14:22:14 -0400
---


I'm not going to say that learning the programming language of [Ruby](http://https://en.wikipedia.org/wiki/Ruby_(programming_language)) was easy.  I have learned different programming languages from the past in high school such as [FORTRAN](https://groups.engin.umd.umich.edu/CIS/course.des/cis400/fortran/fortran.html) and in college I completed statistics courses with [Ada](https://en.wikipedia.org/wiki/Ada_(programming_language)) and [Pascal](http://https://en.wikipedia.org/wiki/Pascal_(programming_language)). All those programming languages take time to learn and to understand the concepts.  I forgot over the years that with any programming language syntax is very important.  Also to be patient with myself and walk away from the computer when needed.  Not that I would hit my computer or get so frustrated that I would yell at the screen.  I am a person that does not like to give up and I take not just hours but even a couple of days to figure out an answer to why my program is not working.  Maybe I need to learn to reach out a little more quicker?

![PopKey](https://m.popkey.co/3d9d6b/K6o6m.gif)

I have learned most importantly that researching in [Google](http://https://www.google.com/) is a must and can help immensely.  When I can't find the answer there, then I can reach out to my peers or the instructors.  It's not a bad thing to do, but I tend to be stubborn and I want to find the answer on my own.  I have found that reaching out to others to help me is actually awesome!  I get to learn from others and their thought processes of why it works the way it works.

I have learned in the lessons in "Intro to Ruby Developement" that I do have an analytical mind.  I am proud of this first month that I got to program in Ruby a tic-tac-toe game and I got it to work!  I did figure out on my own some of the lessons and what a nice feeling!  I do like to attend the study groups and it's beneficial because I learn from others.  A couple things that I have learned from the study groups are that I shouldn't compare myself and that I got this!

The tic-tac-toe lessons were fun and frustrating.  I can explain in the examples below with a couple of snippets of code in Ruby:

```
def valid_move?(board, index)
  if index > 0
    index-1
  end
  if index > 8
    false
  elsif position_taken?(board, index)
    false
  else
    true
  end
end

def position_taken?(board, index)
  if board[index] == " " || board[index] == "" || board[index] == nil
    false
  else board[index] == "X" || board[index] == "O"
    true
  end
end
```
The code above is what I came up with originally and it worked.  The only thing is that it takes up 20 lines.  

I needed help with some code in one of my last lessons before going into the Git and GitHub lessons in my curriculum.  I was just so stuck and the nice instructor walked me through my 50,000 lines and reduced them to five lines.  Maybe I exaggerate, but it felt like wow! Many lines reduced to a few.

Anyway, below is a snippet of the same code (#valid_move? method), but in reduced lines:

```
def valid_move?(board, index)  
  index.between?(0, 8) && position_taken?(board, index)  
end                                                      
```

I know that with time I can get better at how to be more succinct and concise with writing code.  To compare with the #valid_move method in the first example and the second, I took the #index.between? method to help find the position on the tic-tac-toe board between the values of 0 and 8.  The person that plays the game will be asked to input 1 through 9.  The program will then take the input and translate to the appropriate index.  For example index 0 would equal to input 1, index 1 would equal to input 2, index 2 would equal to 3 and so forth. My brain had to think about that for a few moments when I started writing the code.

The '&&' (double ampersands) is a logical operator and in the #valid_move method includes the #position_taken? method.  The second example does not need the if/else or false/true because it is written that the #valid_move? method will be true if the conditions within that method are met, otherwise it will be false. So the #valid_move method is going through each index to find if there is an empty spot with neither an 'X' or 'O' and if these conditions are met then the move is valid.  

I do know that I still have a lot to learn.  I am proud of where I am in this first month.  I look forward to learning more from the lessons, from my peers and from my instructors.  I have learned that I can reach out for help and I don't have to get frustrated as much!  



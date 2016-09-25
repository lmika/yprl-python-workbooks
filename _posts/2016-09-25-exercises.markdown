---
layout: post
title:  "Exercises"
date:   2016-09-25 10:00:00
categories: exercises
---

# Exercises

As you may or may not be aware, I will be away for Saturday 1st October so there will be no session
that day.  In leau of that, I've put togeather the following challanges which you can look at for the
next lesson.

The challenges are set in order of difficulty, and you'll need to complete the first challenge before
moving onto the next one.  Please do as much as you can; but if you get stuck, don't worry: we'll go
through each one in turn during next session.

The next session will be Saturday 8th October at 2:30 pm.

Thanks,

Leon

## Reading Material

The [Python](https://www.python.org/) website has a reasonably good [tutorial](https://docs.python.org/3/tutorial/index.html)
which covers features of the language and how to use the interpretor.

In order to complete the challenges, please do the following:

1. [Download Python 3](/yprl-python-workbooks/resources/) onto your computer.  You could use the
    [scratchpad](/yprl-python-workbooks/scratchpad/) if you really want but it would be good
    practice to get some experience with the real Python program.
2. Read the following sections of the [tutorial](https://docs.python.org/3/tutorial/index.html):
    - 1 to 3.1.2 (this covers most of what we talked about up to date)
    - 3.2 on the `while` loop, especially point 2 and 3
    - 4.1 on the `if` statement

Follow the tutorial and try out the code samples.  Do as much experiementation as you want.  Then, try to work
through the following challenge: 

## A Guessing Game

We're going to build a guessing game that will give the player 5 rounds to guess a number from 1
to 10.  In each round a new number will be chosen and the player will be asked to guess what that
number is.  If they get it right, the win a point.  At the end of the 5 rounds, the player's score
will be displayed.


## Stage 1: Generating a random number

First, you will start with a program which will generate and print a random number.
The way to do that in Python is the following:

    from random import *

    num = randrange(10) + 1
    print("A random number between 1 and 10 is", num)

There are a few concepts introduced here that are explained below (don't worry, you don't need to
know a lot about it now):

1. The `from random import *` statement makes Python aware on how to generate random numbers.
   Don't worry too much on what this is: just include it at the top of your program.
2. The `randrange` function is used to generate random numbers.  It takes a number (integer) and
   returns a random number (also an integer) between 0 and the number given to the function - 1.
   So, if you were to write `randrange(5)` it will return either 0, 1, 2, 3 or 4 (not 5) at
   random.  In this case, the function `randrange(10)` will return a number from 0 to 9 (not 10).
3. Because the `randrange(10)` function returns a random number from 0 to 9, to make the
   random number between 1 and 10, we simply add 1 to the number returned from randrange.
4. Also, the `randrange` function returns a new random number every time we use it, so we'll
   need to store the number in a variable so we can use it later.

Type the program above into Python and run it a few times.  See how the number changes after each
run?  Try to guess what the number will be before running the program and see if you are right.

## Stage 2: Letting The Player Guess

Next, you will 
---
layout: post
title:  "Exercises"
date:   2016-09-25 10:00:00
categories: exercises
---

# Exercises

As you may or may not be aware, I will be away for Saturday 1st October so there will be no session
that day.  In leau of that, I've put togeather the following challange which you can look at for the
next lesson.

The challenge might be a little difficult but please do as much as you can.  If you get stuck,
don't worry: we'll go through it togeather during next session.

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

Try to build a guessing game where the user has to guess a number between 1 and
10.  The way this will work in general is:

1. The program will generate a random number between 1 and 10
2. The user will be asked what the number will be
3. If the user guesses too high, the program will print "Too high"
4. If the user guesses too low, the program will print "Too low"
5. If the user guesses right, the program will say "Correct"

<iframe src="https://trinket.io/embed/python/691b37d400" width="100%" height="700" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

You can build the program in the following stages:

## Stage 1: Generating a random number

First, start with a program which will generate and print a random number.
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

Do the following to try the program out:

1. Start IDLE.  It should be in the start menu.
2. Click "New File" in the "File" menu.
3. Type the program above.
4. Save the program by pressing Ctrl and S.
5. Run the program by pressing F5.  The other window should be updated with the output.
 
Type the program above into Python and run it a few times.  See how the number changes after each
run?  Try to guess what the number will be before running the program and see if you are right.

## Stage 2: Letting The Player Guess

Next, change the program to ask the user to make a guess as to what *num* is.  If the user
is right, print "correct".

HINTS:

1. You will need to `int()` function to convert the user's input value into a number
2. You will need an `if` statement to print "correct" if the user's number is the same as `num`.
3. You will need the `==` to test whether the user's entered number equals with `num`

## Stage 3: Printing Too High and Too Low

Next, see if you can extend your if statement to print out whether the number is too high or too low.

HINTS:

1. You will need the `<` to check to see if the guess is too low
2. You will need the `>` to check to see if the guess is too high
3. You will need to add an `elif` and a `else`

## Extra Credit: Asking Three Times

Next, see if you can ask the user if they can guess the number three times.  Don't worry about
asking the user two more times if they get it right during the first go: we'll discuss how we
could adjust it maybe in the next sesson, and definitely the one after.

HINTS:

1. You will need a `while` loop and another variable to store how many times the user has guessed
   (maybe call it `guessCount` which stands for "guess count").  Also remember to set it to `1`.
2. You might need to move the `while` loop before the first `if`.  If will need to test to see
   if `guessCount` is less than or equal to 3.
3. You will need to use `guessCount = guessCount + 1` somewhere.
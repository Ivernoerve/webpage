---
title: "Wordle solver"
date: 2022-11-14T10:55:17+01:00
draft: false
imgpath: wordle.jpeg
git: https://github.com/Ivernoerve/wordle_solver
---

Wordle is a game similar to mastermind, in which you have guess the right word (sequence of letters). It also happens to be a favorite acticity when procrastinating. Having solved it a few times I wanted to create a program to solve it for me. Thus the work towards a wordle solver began.

<!--more-->
## Approaching it mathematically
 For those who doesn't know; wordle is a game just like mastermind where you guess five letter words until you find the correct one. As you guess you get a response for each index if the letter is not in the word (gray), if the letter is present but at the wrong index (yellow) or if the letter is present and at the correct index (green). Given a dictionary of five letter words we have to sort the letters by a score from best to worst guess at any time given our knowledge of (non)present letters. This is where math comes in, or more precisely statistics, the first step is to find the frequency of each letter in every word in the dictionary. This gives us information about which letters are good guesses (the more often the letter occurs in a word the more likely we are to get a good response). A score for each word can now be given as the sum of the letter frequency of each letter in the word, making it possible to sort it from best to worst (highest to lowest sum). This simple method however has one major flaw, it does not account for double (or triple) letters in a word which is bad since a good guess should span as many unique high frequent letters as possible. Thus a better scoring system would be the sum of the letter frequency of each UNIQUE letter in the word, penalizing words with reccuring letters in them.



## Communicating with the browser 
The program must be able to interact with the browser, so that it can insert guesses, remove invalid guesses, and get the responses for accepted guesses. This was acchieved with the selenium webdriver package, with a script.
The program must be able to interact with the browser, so that it can insert guesses, remove invalid guesses, and get the responses for accepted guesses. This was acchieved with the selenium webdriver package by writing a general class _Browser_  for general webpage interaction i.e; input words, select elemenents etc...
https://iver.noerve.com/projects/wordle_solver/
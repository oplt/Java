Hangman
Hangman is a word-guessing game. It keeps asking the user to guess characters until:

They guess every character correctly (win).

They miss 6 guesses (loss).


Choose a random word

public static String[] words = {"ant", "baboon", "badger", "bat", "bear","beaver", "camel", "cat", "clam", "cobra", "cougar", "coyote", "crow", "deer", "dog", "donkey", "duck", "eagle", "ferret", "fox", "frog", "goat", "goose", "hawk", "lion", "lizard", "llama", "mole", "monkey", "moose", "mouse", "mule", "newt", "otter", "owl", "panda", "parrot", "pigeon", "python", "rabbit", "ram", "rat", "raven","rhino", "salmon", "seal", "shark", "sheep", "skunk", "sloth", "snake", "spider", "stork", "swan", "tiger", "toad", "trout", "turkey","turtle", "weasel", "whale", "wolf", "wombat", "zebra"};

Your game must choose a random word from this list of words.

The placeholders '_' in your game must reflect the number of characters in that word.



Show the gallows
At every turn, you need to show the gallows.

Each String in the array reflects the number of times the user guessed incorrectly.

 public static String[﻿] gallows = {
    "+---+\n" +
    "|   |\n" +
    "    |\n" +
    "    |\n" +   //if the user didn't miss any guesses.
    "    |\n" +
    "    |\n" +
    "=========\n"﻿,

    "+---+\n" +
    "|   |\n" +
    "O   |\n" +   //if the user missed one guess.
    "    |\n" +
    "    |\n" +
    "    |\n" +
    "=========\n"﻿,

    "+---+\n" +
    "|   |\n" +
    "O   |\n" +    //if the user missed two guesses.
    "|   |\n" +
    "    |\n" +
    "    |\n" +
    "=========\n"﻿,

    " +---+\n" +
    " |   |\n" +
    " O   |\n" +   //if the user missed three guesses.
    "/|   |\n" +
    "     |\n" +
    "     |\n" +
    " =========\n"﻿,

    " +---+\n" +
    " |   |\n" +
    " O   |\n" +
    "/|\\  |\n"﻿+   //if the user missed four guesses.
    "     |\n" +
    "     |\n" +
    " =========\n"﻿,

    " +---+\n" +
    " |   |\n" +
    " O   |\n" +
    "/|\\  |\n" +  //if the user missed five guesses.
    "/    |\n" +
    "     |\n" +
    " =========\n"﻿,

    " +---+\n" +
    " |   |\n" +
    " O   |\n" +
    "/|\\  |\n" +   //if the user missed six guesses.
    "/ \\  |\n" +
    "     |\n" +
    " =========\n"﻿}﻿;
You need to show the gallows at every turn. This should be your output when the user misses two guesses.



Show the missed guesses
You need to keep track of every incorrect guess the user made. This helps the user not make the same mistake twice.


Replace placeholders with correct guesses
When the user guesses correctly, replace the matching placeholders.



If the user wins:
Stop the game.


If the user loses:
Stop the game.




Aesthetics:
Add one \n after printing the word/placeholders.

Add two \n after printing the misses.

Add one \n after the guess.




Hints:

Convert a String to an array of characters.

Get the index of a character in a String.

Loop through characters in a String.

check if two arrays are equal to each other.

Possible design:

There are many ways to build Hangman. Here's a possible design for your functions:

randomWord(): returns a random word from the list of random words.

checkGuess(): returns true if the user guessed a letter from the word correctly.

updatePlaceholders(): updates the placeholders when the user makes a correct guess.

printPlaceholders(): prints the placeholders.

printMissedGuesses(): prints guesses that the user missed.

Good luck!

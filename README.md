# constructor-Hangman
About this project
This project is a command line version of the classic Hangman game. This game uses similar logic to the browser-based Hangman game I created, but with this game, I created a command line version using Javascript constructor functions to create letter and word objects, the inquirer npm package to prompt users to guess a letter, and Node.js to run the Javascript code from the command line. For more information on how this project was constructed and put together, see Structure of the project.

Getting started
To play the game from your computer and/or contribute to this project, perform the following steps:

Clone the repository
Install Node.js
Install the dependencies
Clone the repository
The first step is to clone the project repository to a local directory on your computer. To clone the repository, run the following commands:
 git clone https://github.com/rupali8086/constructor-hangman.git
  cd constructor-hangman

  Structure of the project
After you clone the repository, navigate to the project root directory (constructor-hangman). The project directory structure is set up as follows:

Letter.js: Contains a constructor, Letter. This constructor displays an underlying character or a blank placeholder (underscore), depending on whether or not the user has guessed the letter. This constructor includes:

A string value to store the underlying character for the letter.
A boolean value that stores whether that letter has been guessed yet by the user.
A function that returns the underlying character if the letter has been guessed, or a placeholder (underscore) if the letter has not been guessed.
A function that takes a character as an argument and checks it against the underlying character, updating the stored boolean value to true if it was guessed correctly
Word.js: Contains a constructor, Word that depends on the Letter constructor. This is used to create an object representing the current word the user is attempting to guess. The constructor includes:

An array of new Letter objects representing the letters of the underlying word.
A function that returns a string representing the word. This calls the function on each letter object (defined in Letter.js) that displays the character or an underscore and concatenates those together.
A function that takes a character as an argument and calls the guess function on each letter object (defined in Letter.js).
index.js: The file containing the logic for the course of the game, which depends on Word.js and:

Randomly selects a word and uses the Word constructor to store it.
Prompts the user for each guess and keeps track of the user's remaining guesses.
package.json: Lists the project dependencies (third party npm packages) and their version numbers.
.gitignore: Any file or directory listed inside this file will not be tracked by GitHub when code is committed.
package-lock.json: Dependency tree for the project. Lists all the dependencies and their versions.
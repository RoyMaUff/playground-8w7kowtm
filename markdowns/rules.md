# Rules

## Course rules

This is a learning course. Please do not cheat reading the solution provided at the end.  

## MasterMind rules

The real rules involves 2 players and colors pawns. One player becomes the codemaker, the other the codebreaker.  

In this implementation, the script will act as the codemaker and provide informations to help the codebreaker.  
Instead of using colors pawns, we will use numbers between 0 and 9.

The codemaker (the script) chooses a pattern of 4 random digits. Duplicates are allowed, so the random generation could even lead the same four digits.  

The codemaker asks the codebreaker to guess the code.
The codebreaker has 10 tries, if he can not find the code, the codemaker win the game.
If the code is found in less or exactly 10 tries, the codebreaker win the game.

For each tries, the codemaker must provide some informations:

- if one or many guessed digits are correct and are in the right position.
- if one or many guessed digits are correct but are in a wrong position.

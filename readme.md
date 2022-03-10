# Milestone 1 project

### Problem Statement
Create a Tic Tac Toe game. You are free to use any IDE you like.

Game requirements:
* 2 players should be able to play the game (both sitting at the same computer)
* The board should be printed out every time a player makes a move
* You should be able to accept input of the player position and then place a symbol on the board

### Creating the solution 

#### Make a board
* To create a list to store the tokens on the board.
* With this assumption in place, the only valid position to place token are range(0,9)
    * note the range is inclusive of indices 0 and 9.
* Finally, We need to generate a figure for the board


#### Players Select tokens 
* Prompt players to select a token, the token tokens are ('X', 'O'). Other tokens can be used
  * If a player1 selects X
  * Player 2 automatically becomes O

#### Determine the first player
* In order to make the game fair, a random number we be used to determine the first player
 * Best of 2 of 3 attempts, in a random guessing game will determine the winner
 * Players guess a number with a small range 
 * the closest player within a range of +/- 10 to the random number wins the round
 
#### Place Player Tokens on the board
* Prompt each player for a index to place their token on the board
* A player cannot have a consecutive turn. This means player1 cannot play then player 1 plays immediately after again 
    * player turn must alternate
* Edge Cases:
    * If the provided index is occupied, prompt the current player for another location to place their token.
    * If the provided index is out of bound, prompt current player for another location.
        * Valid bound is 0 <= index <= 9
    * Else
        * Add player turn on that location
     
#### Determine the game status 
* After placing a token on the board, game status must always be verified.
* The game can end as a DRAW, TIE OR LOSS
    * Condition for a TIE:
        * if the board is filled and no player has matching tokens.
    * Conditions for a Win:
        * A game is won, if a player has a matching patterns horizontally, vertically or diagonally.
        * The board does not have to be completed filled for a game to be WON.
    * Conditions for a LOSS:
        * A game is loss, if a player has a matching pattern.
        * The board does not have to be completely filled for a game to be LOST.
            
#### Prompt Players to restart the game
* After a round is completed, prompt user to restart the game
* A round is completed if:
    * if the game status is a WIN, LOSS or TIE
* Conditions for restarting the game
    * if a player answers no => exit the game
    * else if both players answer yes => continue

### What I Learnt

### Resources



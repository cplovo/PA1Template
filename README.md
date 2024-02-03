# CS 212 - Programming Assignment 1

Design Due: Friday 02/09
Final Due: Friday 02/16

## Summary

For this assignment you will use Class to develop a Simplified UNO game.

## Description

UNO is a card game played with a standard deck, aiming to be the first to get rid of all cards. Players match cards by number or color, using action cards to disrupt opponents. Wild cards add unpredictability, allowing color choice. The game ends when a player empties their hand, and points are scored based on opponents' remaining cards.

_Simplified Version UNO:_ In a Simplified UNO Game, there are four colors: red, blue, green, and yellow. Each color has cards numbered from 0 to 9. In this version of the game you are making, there is no Skip, Reverse, Draw Two, Draw Four, or Wild Cards. So **Your Deck Will be 60 Cards total.**


_Special Action Cards (Stretch Goal):_ There are also special action cards such as Skip, Reverse, and Draw Two. There are eight Skip cards (two in each color), eight Reverse cards (two in each color), and eight Draw Two cards (two in each color). These action cards allow players to skip turns, reverse the order of play, and force opponents to draw two cards, respectively.
Additionally, there are four Wild (color-change) cards and four Wild Draw Four cards in the deck.

A standard Uno deck consists of 108 cards.

### Scoring

In Uno, scoring occurs at the end of each round, and the player who first empties their hand receives points based on the cards remaining in opponents' hands.

The scoring system is as follows:

- Number cards (0-9): Face value (e.g., a "7" is worth 7 points).
- Action cards (Skip, Reverse, Draw Two): 20 points each (not needed unless doing stretch goal).
- Wild cards (color-change), Wild Draw Four: 50 points each (not needed unless doing stretch goal).

Players keep a running total of the points they accumulate in each round. The game typically continues until one player reaches a designated point threshold (e.g., 500 points), and that player is declared the overall winner.

### Game play

1. Each player is dealt seven cards at the start of the game.
2. A card from the draw pile is turned over to begin the discard pile.
3. Players take turns matching the top card of the discard pile by color or number.
4. Players must say "Uno" when they have one card left; failing to do so may result in a penalty.
5. Wild cards allow players to change the color in play, and Wild Draw Four cards force the nextplayer to draw four cards.
6. If a player cannot play a card, they must draw from the draw pile until they get a playable card.
7. The game continues until one player has no cards left.
8. Points are awarded based on the remaining cards in opponents' hands.
9. The first player to reach a set amount of points (e.g., 200) is declared the winner.

## Assignment Details

1. Develop a simplified version of the Uno card game, excluding the use of wild cards, skip, reverse, and draw two actions.
2. The game should involve two or more players. Each player is dealt seven cards at the beginning of the game, and a discard pile is initiated with a card drawn from the deck.
3. Players take turns playing cards from their hand, matching either the color or number of the top card in the discard pile. The objective is to be the first to play all cards.
4. Special action cards like skip, reverse, and draw two are omitted from this version.
5. Players must announce 'Uno' [printed out to the console] when they have one card left to avoid penalties. The game continues until a player successfully discards all cards.
6. Points are awarded based on opponents' remaining cards.
7. The first player to reach a specified point threshold, such as 200, is declared the winner.

8. Create a program in Java to implement and simulate this simplified Uno game, defining appropriate classes and methods for game mechanics."

Beside the client class Main which contains only the `main()` method, you must to create another **class** named **Hand**. It is up to you how to design and implement the **Hand** class. However, it should have the following minimum requirements:

### Data Members

1. Number of card(s) in the hand.
2. Content (including color) of all the cards in the hand.

### Methods

1. A constructor to instantiate a hand.
2. `initializeGame()`: Initializes the game, creates players, and shuffles the deck.
3. `dealInitialCards()`: Deals an initial set of cards to each player.
4. `startGame()`: Initiates the game loop and controls the flow of turns between players.
5. `displayGameState()`: Prints the current state of the game, including the top card on the discard pile and each player's hand.
6. `getPlayerMove()`: Prompts the current player to choose a card to play or draw from the deck.
7. `playCard()`: Handles the logic for playing a card and updating the discard pile.
8. `drawCard()`: Handles the logic for drawing a card from the deck.
9. `checkUno()`: Checks if a player has one card left and prompts them to say "Uno."
10. `checkWinner()`: Determines if a player has won and ends the game.
11. `printWinner()`: Prints the winner of the game.

### NOTE:
These methods cover the core functionality of managing the game, player actions, and determining the winner. _**Depending on your implementation, you may need additional methods to handle specific game rules and actions.**_

## Sample Runs

Here is an example of how program should work:

```
RUN 1:

Welcome to Uno!

Player 1's turn:
Your hand: [Red 5, Yellow 8, Green 2, Blue 7]
Top card: Blue 3
Choose a card to play: Green 2

Player 2's turn:
Your hand: [Yellow 8]
Top card: Green 2
Choose a card to play: Yellow 8

Player 1's turn:
Your hand: [Red 5]
Top card: Yellow 8
Choose a card to play: Red 5

Player 1 wins!

Thanks for playing Uno!

```

---

```
RUN 2

Welcome to Uno!

Player 1's turn:
Your hand: [Red 3, Yellow 2, Green 9, Blue 1]
Top card: Blue 7
Choose a card to play: Green 9

Player 2's turn:
Your hand: [Red 3, Yellow 2, Blue 1]
Top card: Green 9
Choose a card to play: Red 3

Player 1's turn:
Your hand: [Yellow 2, Blue 1]
Top card: Red 3
Choose a card to play: Yellow 2

Player 2's turn:
Your hand: [Blue 1]
Top card: Yellow 2
Choose a card to play: Blue 1

Player 1's turn:
Your hand: []
Top card: Blue 1
Player 1 wins!

Thanks for playing Uno!

```


## Submission

### Part 1 (10 points): Design and test cases.

No code is required for the design.

To GitHub:

- In design.txt, a description of what is in your **Hand** class. The description should include:
  - data type of the data
  - return type and list of parameters(if any) for the constructor(s) and methods
  - an algorithm for **all your proposed methods** given the choices made for your data members.


### Part 2 (40 points): Final Product

**To GitHub:**

- All coded needed to run your program.
  - Reminders: Don't forget to include header comments and appropriate JavaDoc

**To Moodle:** 
- A file, reflection.txt, containing answers to at least the following:
  - What is the most challenging thing you experienced?
  - How did you overcome it?
  - Anything you would do differently given what you know now.
  - What did you like about working with classes and what was difficult?
  - How you felt about the step up in difficulty between this and PA0.


### Stretch Goal (7 Extra Credit points on the next Quiz):
Make a version of the Uno Game, but with the Special Action Cards of Skip, Reverse, Draw 2, Wild Card (change color), and Wild Card draw 4 (Change color + next turn player has to draw 4 cards).

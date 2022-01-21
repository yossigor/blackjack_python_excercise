# Blackjack in python

## Game Loop

```python
while player.chips:
    # Create new deck and shuffle.
    # Take a bet from the player.
    # Deal two cards for the player.
    # Deal two cards for the dealer.
    # Check for Blackjack
    while go_on:
        # Display relevant actions for the player.
        # Player chooses an action.
        # Perform operation on chips
        # Perform operation cards
    if not(player.bust)
        # Dealer plays strategy
    # Calculate winner
    # Calculate chips
    # Display result
```

## Classes suggestion

### Card

Represents a card in the Blackjack game.

#### Fields

1. `suit`
2. `rank`
3. `is_face`: Is the card visible or not.

#### Methods

1. `__init__`: Creates a card with given parameters.
2. `__repr__` or `__str__`: Converts the card to a string.
3. `show`: Prints the card representation to the console.  

### Deck

A deck consisting of 52 cards packs. 

#### Fields

1. `num`: Number of normal 52 cards packs in the deck.
2. `cards`: List of `Card`s.

#### Methods

1. `__init__`: Creates a deck with given parameters.
2. `__repr__` or `__str__`: Converts the deck to a string.
3. `__len__`: Number of cards in the deck.
4. `build`: Combines all the packs to one deck.
5. `shuffle`: Shuffles the list of cards.
6. `draw`: Gets the top card and removes it from the deck. 

### Chips

Represents the current players chips.

#### Fields

1. `amount`: Number of chips the player has.

#### Methods

1. `bet`: Takes chips from the player and puts them in the pot.
2. `receive`: Adds chips to the player.

### Hand

#### Fields

1. `cards`: List of cards.

#### Methods

1. `score`: Calculates the hand score.
2. `add_card`: Adds card to the hand.
3. `__repr__` or `__str__`: Converts the hand to a string.

### User

#### Fields

1. `hand`: The user's current hand.

### Player(User)

#### Methods

1. `valid_actions`: Calculate the valid player's actions.
2. `play`: Play an action. Calculate the state of the player after the action.

### Dealer(User)

#### Methods

1. `play_strategy`: Plays the dealer hand according to Blackjack rules.

### Game

#### Fields

1. `winner`: Current turn winner.
2. `pot`: The current bet.

#### Methods

1. `__init__`: Initialize the game.
2. `play`: Starts the game loop.



## Test Driven Design

In this excercise we will focus on testing our code on the fly.

### Workflow

Repeat the following actions:
1. Add a test.
2. Run the tests. New tests should fail.
3. Write the simplest and minimal change to pass the tests.
4. Run the tests. All tests should pass.
5. Refactor:
    * Moving code to where it most logically belongs.
    * Remove code duplications.
    * Make names self documenting.
    * Split methods into smaller pieces.
6. Run the tests. All tests should pass.

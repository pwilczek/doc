# Problem
We'd like to model __Deck of Cards__ in our app and prepare __shuffled set of cards__ for a play.
So:
* cards are shuffled (random order)
* each card has a position in a pile
* we can get a card by its position (we get random one)
* all 52 cards (no more, no less) are in a pile after shuffling

![Deck of Cards](./img/pile-of-cards.png "Pile of Cards")

## Standard deck of cards
_The standard 52-card deck of French-suited playing cards is the most common pack..._ [Wiki](https://en.wikipedia.org/wiki/Standard_52-card_deck)
![Deck of Cards](./img/deck-of-cards.png "Deck of Cards")

| Ranks | Suits        |
|-------|--------------|
| 2     | Clubs |
| 3     | Diamonds |
| 4     | Hearts |
| 5     | Spades |
| 6     |  |
| 7     |  |
| 8     |  |
| 9     |  |
| 10    |  |
| Jack  |  |
| Queen |  |
| King  |  |
| Ace   |  |

## Tech details
* after shuffling we'd want to save the result in H2 (already set)
* shuffling happens after calling a link below
* for simplicity, let's assume we only support single game (shuffling clears old deck)
* card is returned by its position via provided link
* getting a card by position is stable (get position 42 returns the same card until deck is reshuffled)

## Link for the game
[Shuffle the cards](http://localhost:8080/shuffle)

[Get a card](http://localhost:8080/card/42)
## Some hints
[H2 Console](http://localhost:8080/h2-console)

__Change JDBC URL to:__ jdbc:h2:mem:doc

__User/pass:__ doc

![H2 Console](./img/h2-console.png "H2 Console")

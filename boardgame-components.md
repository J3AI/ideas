Schema:

User
has_many usergames
has_many games through usergames

UserGames
belongs_to user
belongs_to game

Game
has_many usergames
has_many users through usergames
has_one board
has_many decks
has_many token_sets
has_many counters
has_many dice? (possibly just do this through chat)

Board
belongs_to game

Deck
belongs_to game
has_many cards

Card
belongs_to deck

TokenSet
belongs_to game
has_many tokens

Token
belongs_to token_set

Counter
belongs_to game


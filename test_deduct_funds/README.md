# test_deduct_funds

The game's price is deducted from the buyer's wallet.

Reads `current_user_accounts.txt` and `available_games.txt` from the project root.

## success

player_one buys Dungeon Delve ($35.50): balance drops from $200.00 to $164.50.

## failure

player_one tries to buy Dungeon Delve from ghost_seller, who does not exist: balance stays $200.00.

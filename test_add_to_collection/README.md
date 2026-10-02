# test_add_to_collection

The purchased game is added to the user's game collection.

Reads `current_user_accounts.txt` and `available_games.txt` from the project root.

## success

player_one buys Pixel Quest from seller_sam: it is added to the collection.

## failure

player_one tries to buy Moon Miners, which is not for sale: nothing is added to the collection.

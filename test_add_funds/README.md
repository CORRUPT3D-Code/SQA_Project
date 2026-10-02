# test_add_funds

The game's price is added to the seller's wallet.

Reads `current_user_accounts.txt` and `available_games.txt` from the project root.

## success

player_one buys Space Raiders from seller_sam: seller_sam is credited $20.00.

## failure

player_one tries to buy Space Raiders from buyer_bea, who is not selling it: no funds are added to anyone.

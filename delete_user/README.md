# delete_user

Admin deletes an existing user who is not the current user; the user's games are cancelled and no further transactions are accepted on them.

Reads `current_user_accounts.txt`, `available_games.txt` and `game_collection.txt` from the project root.
Accounts: admin = meow_meow_17 (AA, $500.00), full_standard = player_one (FS, $200.00), buy_standard = buyer_bea (BS, $50.00), sell_standard = seller_sam (SS, $1000.00).

## admin/success

Admin deletes seller_sam, then tries to buy seller_sam's Space Raiders: the buy is rejected.

## admin/failure

Admin tries to delete ghost_user, who does not exist: rejected.

## full_standard/success

Full-standard user player_one enters delete: rejected immediately with no prompts, and the session continues to a normal logout.

## full_standard/failure

Full-standard user player_one enters delete and then types its inputs anyway (buyer_bea): delete is rejected, each extra line is rejected as an unknown command, and nothing is saved.

## buy_standard/success

Buy-standard user buyer_bea enters delete: rejected immediately with no prompts, and the session continues to a normal logout.

## buy_standard/failure

Buy-standard user buyer_bea enters delete and then types its inputs anyway (buyer_bea): delete is rejected, each extra line is rejected as an unknown command, and nothing is saved.

## sell_standard/success

Sell-standard user seller_sam enters delete: rejected immediately with no prompts, and the session continues to a normal logout.

## sell_standard/failure

Sell-standard user seller_sam enters delete and then types its inputs anyway (buyer_bea): delete is rejected, each extra line is rejected as an unknown command, and nothing is saved.

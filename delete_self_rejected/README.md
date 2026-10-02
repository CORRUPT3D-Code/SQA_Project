# delete_self_rejected

An admin cannot delete the account they are currently logged in as.

Reads `current_user_accounts.txt`, `available_games.txt` and `game_collection.txt` from the project root.
Accounts: admin = meow_meow_17 (AA, $500.00), full_standard = player_one (FS, $200.00), buy_standard = buyer_bea (BS, $50.00), sell_standard = seller_sam (SS, $1000.00).

## admin/success

Admin deletes a different user, buyer_bea: accepted.

## admin/failure

Admin tries to delete meow_meow_17 (themselves): rejected.

## full_standard/success

Full-standard user player_one enters delete: rejected immediately with no prompts, and the session continues to a normal logout.

## full_standard/failure

Full-standard user player_one enters delete and then types its inputs anyway (player_one): delete is rejected, each extra line is rejected as an unknown command, and nothing is saved.

## buy_standard/success

Buy-standard user buyer_bea enters delete: rejected immediately with no prompts, and the session continues to a normal logout.

## buy_standard/failure

Buy-standard user buyer_bea enters delete and then types its inputs anyway (buyer_bea): delete is rejected, each extra line is rejected as an unknown command, and nothing is saved.

## sell_standard/success

Sell-standard user seller_sam enters delete: rejected immediately with no prompts, and the session continues to a normal logout.

## sell_standard/failure

Sell-standard user seller_sam enters delete and then types its inputs anyway (seller_sam): delete is rejected, each extra line is rejected as an unknown command, and nothing is saved.

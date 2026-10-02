# delete_not_admin_rejected

Someone logged in as a non-admin should not be able to use delete.

Reads `current_user_accounts.txt`, `available_games.txt` and `game_collection.txt` from the project root.
Accounts: admin = meow_meow_17 (AA, $500.00), full_standard = player_one (FS, $200.00), buy_standard = buyer_bea (BS, $50.00), sell_standard = seller_sam (SS, $1000.00).

## admin/success

Admin deletes player_one: accepted.

## admin/failure

Admin deletes player_one, then tries to delete player_one again: the second delete is rejected because the user no longer exists.

## full_standard/success

Full-standard user player_one enters delete: rejected, but the session carries on and an allowed addcredit of $10.00 is accepted.

## full_standard/failure

Full-standard user player_one enters delete: rejected immediately, no username prompt.

## buy_standard/success

Buy-standard user buyer_bea enters delete: rejected immediately with no prompts, and the session continues to a normal logout.

## buy_standard/failure

Buy-standard user buyer_bea enters delete and then types its inputs anyway (player_one): delete is rejected, each extra line is rejected as an unknown command, and nothing is saved.

## sell_standard/success

Sell-standard user seller_sam enters delete: rejected immediately with no prompts, and the session continues to a normal logout.

## sell_standard/failure

Sell-standard user seller_sam enters delete and then types its inputs anyway (player_one): delete is rejected, each extra line is rejected as an unknown command, and nothing is saved.

# test_create_rejected

A standard user cannot perform the privileged create transaction.

Reads `current_user_accounts.txt`, `available_games.txt` and `game_collection.txt` from the project root.
Accounts: admin = meow_meow_17 (AA, $500.00), full_standard = player_one (FS, $200.00), buy_standard = buyer_bea (BS, $50.00), sell_standard = seller_sam (SS, $1000.00).

## admin/success

Admin creates fresh_player (sell-standard): accepted.

## admin/failure

Admin tries to create a user named END, which is reserved as the end marker of the accounts file: rejected.

## full_standard/success

Full-standard user player_one enters create: rejected, but the session carries on and an allowed addcredit of $10.00 is accepted.

## full_standard/failure

Full-standard user player_one enters create: rejected immediately and nothing is saved for a new user.

## buy_standard/success

Buy-standard user buyer_bea enters create: rejected immediately with no prompts, and the session continues to a normal logout.

## buy_standard/failure

Buy-standard user buyer_bea enters create and then types its inputs anyway (fresh_player, sell-standard): create is rejected, each extra line is rejected as an unknown command, and nothing is saved.

## sell_standard/success

Sell-standard user seller_sam enters create: rejected immediately with no prompts, and the session continues to a normal logout.

## sell_standard/failure

Sell-standard user seller_sam enters create and then types its inputs anyway (fresh_player, sell-standard): create is rejected, each extra line is rejected as an unknown command, and nothing is saved.

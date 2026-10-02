# test_admin_mode_user_exists

In admin mode, the username entered for addcredit must exist in the system.

Reads `current_user_accounts.txt`, `available_games.txt` and `game_collection.txt` from the project root.
Accounts: admin = meow_meow_17 (AA, $500.00), full_standard = player_one (FS, $200.00), buy_standard = buyer_bea (BS, $50.00), sell_standard = seller_sam (SS, $1000.00).

## admin/success

Admin adds $50.00 to existing user buyer_bea: accepted.

## admin/failure

Admin adds $50.00 to nobody_here, who does not exist: rejected.

## full_standard/success

In standard mode, no username is asked for: player_one's $40.00 goes straight to their own account.

## full_standard/failure

player_one adds $40.00 and then types nobody_here as if asked for a username: the credit still goes to their own account and nobody_here is rejected as an unknown command.

## buy_standard/success

In standard mode, no username is asked for: buyer_bea's $40.00 goes straight to their own account.

## buy_standard/failure

buyer_bea adds $40.00 and then types nobody_here as if asked for a username: the credit still goes to their own account and nobody_here is rejected as an unknown command.

## sell_standard/success

In standard mode, no username is asked for: seller_sam's $40.00 goes straight to their own account.

## sell_standard/failure

seller_sam adds $40.00 and then types nobody_here as if asked for a username: the credit still goes to their own account and nobody_here is rejected as an unknown command.

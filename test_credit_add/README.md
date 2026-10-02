# test_credit_add

In standard mode, addcredit asks only for the amount and adds it to the current user.

Reads `current_user_accounts.txt`, `available_games.txt` and `game_collection.txt` from the project root.
Accounts: admin = meow_meow_17 (AA, $500.00), full_standard = player_one (FS, $200.00), buy_standard = buyer_bea (BS, $50.00), sell_standard = seller_sam (SS, $1000.00).

## admin/success

In admin mode, the admin is asked for the amount and a username; $100.00 added to their own account (meow_meow_17) is accepted.

## admin/failure

Admin enters a non-numeric amount (abc): rejected before the username is asked for.

## full_standard/success

player_one adds $100.00 to their own account: balance $300.00.

## full_standard/failure

player_one enters a non-numeric amount (abc): rejected.

## buy_standard/success

buyer_bea adds $100.00 to her own account: balance $150.00.

## buy_standard/failure

buyer_bea enters an amount with three decimal places (12.345): rejected.

## sell_standard/success

seller_sam adds $100.00 to his own account: balance $1100.00.

## sell_standard/failure

seller_sam enters an amount with a dollar sign ($50): rejected.

# test_admin_mode_credit_add

In admin mode, addcredit asks for the amount of credit to add and the account to add it to.

Reads `current_user_accounts.txt`, `available_games.txt` and `game_collection.txt` from the project root.
Accounts: admin = meow_meow_17 (AA, $500.00), full_standard = player_one (FS, $200.00), buy_standard = buyer_bea (BS, $50.00), sell_standard = seller_sam (SS, $1000.00).

## admin/success

Admin adds $250.00 to player_one: asked for the amount, then the username.

## admin/failure

Admin enters a negative amount (-50.00): rejected before the username is asked for.

## full_standard/success

In standard mode, player_one is asked only for the amount (no username) and $25.00 goes to their own account.

## full_standard/failure

player_one types a username (buyer_bea) where the amount is expected: rejected as an invalid amount, because standard mode only asks for an amount.

## buy_standard/success

In standard mode, buyer_bea is asked only for the amount (no username) and $25.00 goes to their own account.

## buy_standard/failure

buyer_bea types a username (player_one) where the amount is expected: rejected as an invalid amount, because standard mode only asks for an amount.

## sell_standard/success

In standard mode, seller_sam is asked only for the amount (no username) and $25.00 goes to their own account.

## sell_standard/failure

seller_sam types a username (buyer_bea) where the amount is expected: rejected as an invalid amount, because standard mode only asks for an amount.

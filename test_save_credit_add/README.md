# test_save_credit_add

Each accepted addcredit is saved to the daily transaction file as an 06 line.

Reads `current_user_accounts.txt`, `available_games.txt` and `game_collection.txt` from the project root.
Accounts: admin = meow_meow_17 (AA, $500.00), full_standard = player_one (FS, $200.00), buy_standard = buyer_bea (BS, $50.00), sell_standard = seller_sam (SS, $1000.00).

## admin/success

Admin adds $100.00 to seller_sam and $200.00 to buyer_bea: two 06 lines are written.

## admin/failure

Admin enters a non-numeric amount (fifty): rejected and not saved.

## full_standard/success

player_one adds $75.00: an 06 line is written.

## full_standard/failure

player_one enters an amount of 0.00: rejected and not saved.

## buy_standard/success

buyer_bea adds $30.00: an 06 line is written.

## buy_standard/failure

buyer_bea enters a negative amount (-10.00): rejected and not saved.

## sell_standard/success

seller_sam adds $500.00: an 06 line is written.

## sell_standard/failure

seller_sam enters a non-numeric amount (abc): rejected and not saved.

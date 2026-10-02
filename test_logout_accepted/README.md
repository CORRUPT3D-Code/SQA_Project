# test_logout_accepted

Logout writes out the daily transaction file and then accepts no transaction other than login.

Reads `current_user_accounts.txt`, `available_games.txt` and `game_collection.txt` from the project root.
Accounts: admin = meow_meow_17 (AA, $500.00), full_standard = player_one (FS, $200.00), buy_standard = buyer_bea (BS, $50.00), sell_standard = seller_sam (SS, $1000.00).

## admin/success

Admin creates new_gamer and logs out: the 01 and 00 lines are written.

## admin/failure

Admin logs out, then tries create: rejected because only login is accepted after a logout.

## full_standard/success

player_one adds $50.00 and logs out: the 06 and 00 lines are written.

## full_standard/failure

player_one logs out, then tries addcredit: rejected because only login is accepted after a logout.

## buy_standard/success

buyer_bea buys Space Raiders and logs out: the 04 and 00 lines are written.

## buy_standard/failure

buyer_bea logs out, then tries buy: rejected because only login is accepted after a logout.

## sell_standard/success

seller_sam puts Neon Drift up for sale and logs out: the 03 and 00 lines are written.

## sell_standard/failure

seller_sam logs out, then tries sell: rejected because only login is accepted after a logout.

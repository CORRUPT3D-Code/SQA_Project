# test_added_to_DailyTransactionFile

Sell and buy transactions are logged to the daily transaction file when the session ends with logout.

Reads `current_user_accounts.txt`, `available_games.txt` and `game_collection.txt` from the project root.
Accounts: admin = meow_meow_17 (AA, $500.00), full_standard = player_one (FS, $200.00), buy_standard = buyer_bea (BS, $50.00), sell_standard = seller_sam (SS, $1000.00).

## admin/success

Admin performs every transaction type (create, addcredit, refund, buy, sell, delete) and logs out: lines 01, 06, 05, 04, 03 and 02 are written in that order, followed by 00.

## admin/failure

Admin creates new_gamer and buys Space Raiders, but the input ends without a logout: no daily transaction file is written.

## full_standard/success

player_one puts Star Forge up for sale at $25.00 and buys Space Raiders, then logs out: a 03 line, a 04 line and the 00 line are written.

## full_standard/failure

player_one makes the same sell and buy, but the input ends without a logout: no daily transaction file is written.

## buy_standard/success

buyer_bea buys Space Raiders and logs out: the 04 and 00 lines are written.

## buy_standard/failure

buyer_bea buys Space Raiders but the input ends without a logout: no daily transaction file is written.

## sell_standard/success

seller_sam puts Neon Drift up for sale at $30.00 and logs out: the 03 and 00 lines are written.

## sell_standard/failure

seller_sam puts Neon Drift up for sale but the input ends without a logout: no daily transaction file is written.

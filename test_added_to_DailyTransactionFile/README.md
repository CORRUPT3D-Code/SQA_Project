# test_added_to_DailyTransactionFile

Sell and buy transactions are logged to the daily transaction file when the session ends with logout.

Reads `current_user_accounts.txt` and `available_games.txt` from the project root.

## success

player_one puts Star Forge up for sale at $25.00 and buys Space Raiders, then logs out: a 03 line, a 04 line and the 00 line are written.

## failure

player_one makes the same sell and buy, but the input ends without a logout: no daily transaction file is written.

# test_valid_buy_account

Buy is accepted from any account type except sell-standard.

Reads `current_user_accounts.txt`, `available_games.txt` and `game_collection.txt` from the project root.
Accounts: admin = meow_meow_17 (AA, $500.00), full_standard = player_one (FS, $200.00), buy_standard = buyer_bea (BS, $50.00), sell_standard = seller_sam (SS, $1000.00).

## admin/success

Admin meow_meow_17 buys Dungeon Delve: accepted.

## admin/failure

Admin may buy, but tries to buy Dungeon Delve from meow_meow_17 (themselves), who is not selling it: rejected.

## full_standard/success

Full-standard user player_one buys Space Raiders: accepted.

## full_standard/failure

player_one may buy, but tries to buy Dungeon Delve from player_one (themselves), who is not selling it: rejected.

## buy_standard/success

Buy-standard user buyer_bea buys Dungeon Delve: accepted.

## buy_standard/failure

buyer_bea may buy, but tries to buy Space Raiders from buyer_bea (herself), who is not selling it: rejected.

## sell_standard/success

Sell-standard user seller_sam enters buy: rejected, but the session carries on and an allowed sell of Neon Drift at $30.00 is accepted.

## sell_standard/failure

Sell-standard user seller_sam enters buy: rejected immediately.

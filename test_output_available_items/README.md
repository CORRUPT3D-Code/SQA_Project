# test_output_available_items

list prints every game currently for sale with its seller and price.

Reads `current_user_accounts.txt`, `available_games.txt` and `game_collection.txt` from the project root.
Accounts: admin = meow_meow_17 (AA, $500.00), full_standard = player_one (FS, $200.00), buy_standard = buyer_bea (BS, $50.00), sell_standard = seller_sam (SS, $1000.00).

## admin/success

Admin enters list: every game in available_games.txt is printed.

## admin/failure

Admin logs out, then enters list: rejected because only login is accepted after a logout.

## full_standard/success

player_one enters list: all games from available_games.txt are printed.

## full_standard/failure

list before login is rejected.

## buy_standard/success

buyer_bea enters list: every game in available_games.txt is printed.

## buy_standard/failure

buyer_bea logs out, then enters list: rejected because only login is accepted after a logout.

## sell_standard/success

seller_sam puts Neon Drift up for sale, then enters list: Neon Drift is NOT shown, because a new game is not available until the next session.

## sell_standard/failure

seller_sam logs out, then enters list: rejected because only login is accepted after a logout.

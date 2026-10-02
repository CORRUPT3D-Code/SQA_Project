# test_valid_game_price

A game's price can be at most $999.99.

Reads `current_user_accounts.txt`, `available_games.txt` and `game_collection.txt` from the project root.
Accounts: admin = meow_meow_17 (AA, $500.00), full_standard = player_one (FS, $200.00), buy_standard = buyer_bea (BS, $50.00), sell_standard = seller_sam (SS, $1000.00).

## admin/success

Boundary: admin sells Penny Arcade at $0.01, the lowest valid price: accepted.

## admin/failure

Admin enters a non-numeric price (free): rejected.

## full_standard/success

Boundary: player_one sells Galaxy Titans at $999.99: accepted.

## full_standard/failure

player_one tries a price of $1000.00, then a negative price (-5.00): both rejected.

## buy_standard/success

Buy-standard user buyer_bea enters sell: rejected immediately with no prompts, and the session continues to a normal logout.

## buy_standard/failure

Buy-standard user buyer_bea enters sell and then types its inputs anyway (Neon Drift, 15.00): sell is rejected, each extra line is rejected as an unknown command, and nothing is saved.

## sell_standard/success

seller_sam sells Neon Drift at $15.00: accepted.

## sell_standard/failure

seller_sam enters a price with three decimal places (12.345): rejected.

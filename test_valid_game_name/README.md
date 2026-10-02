# test_valid_game_name

A game name for sale can be at most 25 characters long.

Reads `current_user_accounts.txt`, `available_games.txt` and `game_collection.txt` from the project root.
Accounts: admin = meow_meow_17 (AA, $500.00), full_standard = player_one (FS, $200.00), buy_standard = buyer_bea (BS, $50.00), sell_standard = seller_sam (SS, $1000.00).

## admin/success

Boundary: admin sells a game with a one-character name (Q): accepted.

## admin/failure

Admin enters an empty game name (a blank line): rejected before the price is asked for.

## full_standard/success

Boundary: player_one sells The Legend of Pixel Lands (exactly 25 characters): accepted.

## full_standard/failure

player_one sells The Legend of Pixel Islands (27 characters): rejected before the price is asked for.

## buy_standard/success

Buy-standard user buyer_bea enters sell: rejected immediately with no prompts, and the session continues to a normal logout.

## buy_standard/failure

Buy-standard user buyer_bea enters sell and then types its inputs anyway (Mystery of the Old Lights, 22.00): sell is rejected, each extra line is rejected as an unknown command, and nothing is saved.

## sell_standard/success

Boundary: seller_sam sells Mystery of the Old Lights (exactly 25 characters): accepted.

## sell_standard/failure

Boundary: seller_sam sells Mystery of the Old Lighter (26 characters, one over): rejected.

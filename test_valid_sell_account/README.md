# test_valid_sell_account

Sell is accepted from any account type except buy-standard.

Reads `current_user_accounts.txt`, `available_games.txt` and `game_collection.txt` from the project root.
Accounts: admin = meow_meow_17 (AA, $500.00), full_standard = player_one (FS, $200.00), buy_standard = buyer_bea (BS, $50.00), sell_standard = seller_sam (SS, $1000.00).

## admin/success

Admin puts Moon Base up for sale: accepted, because admins can sell.

## admin/failure

Admin may sell, but tries to sell Titan Wars, a name that already exists: rejected.

## full_standard/success

Full-standard user player_one puts Star Forge up for sale: accepted.

## full_standard/failure

player_one may sell, but enters a non-numeric price (abc): rejected.

## buy_standard/success

Buy-standard user buyer_bea enters sell: rejected, but the session carries on and an allowed buy of Space Raiders is accepted.

## buy_standard/failure

Buy-standard user buyer_bea enters sell: rejected immediately.

## sell_standard/success

Sell-standard user seller_sam puts Neon Drift up for sale at $30.00: accepted.

## sell_standard/failure

seller_sam may sell, but enters a price of 0.00: rejected.

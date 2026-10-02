# test_thousand_dollar_limit

At most $1000.00 can be added to an account in a single session.

Reads `current_user_accounts.txt`, `available_games.txt` and `game_collection.txt` from the project root.
Accounts: admin = meow_meow_17 (AA, $500.00), full_standard = player_one (FS, $200.00), buy_standard = buyer_bea (BS, $50.00), sell_standard = seller_sam (SS, $1000.00).

## admin/success

The limit is per account: admin adds $1000.00 to buyer_bea and $1000.00 to seller_sam in the same session, and both are accepted.

## admin/failure

Admin adds $700.00 to player_one (accepted), then $400.00 more to player_one, which would total $1100.00: rejected.

## full_standard/success

Boundary: player_one adds exactly $1000.00: accepted.

## full_standard/failure

player_one adds $600.00 (accepted), then $500.00, which would bring the session total to $1100.00: rejected.

## buy_standard/success

Boundary: buyer_bea adds exactly $1000.00: accepted.

## buy_standard/failure

buyer_bea adds $1000.01, one cent over the limit: rejected.

## sell_standard/success

Boundary across transactions: seller_sam adds $400.00 then $600.00, exactly $1000.00 in total: both accepted.

## sell_standard/failure

seller_sam adds $1000.00 (accepted), then $0.01 more: rejected because the session limit is used up.

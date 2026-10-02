# test_logout_rejected

Logout is only accepted while a user is logged in.

Reads `current_user_accounts.txt`, `available_games.txt` and `game_collection.txt` from the project root.
Accounts: admin = meow_meow_17 (AA, $500.00), full_standard = player_one (FS, $200.00), buy_standard = buyer_bea (BS, $50.00), sell_standard = seller_sam (SS, $1000.00).

## admin/success

Admin user meow_meow_17 logs in and logs out: the logout is accepted.

## admin/failure

logout before any login is rejected; after a valid login and logout, a second logout is also rejected.

## full_standard/success

player_one logs in and logs out: the logout is accepted.

## full_standard/failure

logout before any login is rejected; after a valid login and logout, a second logout is also rejected.

## buy_standard/success

Buy-standard user buyer_bea logs in and logs out: the logout is accepted.

## buy_standard/failure

logout before any login is rejected; after a valid login and logout, a second logout is also rejected.

## sell_standard/success

Sell-standard user seller_sam logs in and logs out: the logout is accepted.

## sell_standard/failure

logout before any login is rejected; after a valid login and logout, a second logout is also rejected.

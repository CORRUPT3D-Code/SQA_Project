# test_login_rejected

Logins and transactions are rejected when invalid: an unknown username, any transaction before login, or a second login while already logged in.

Reads `current_user_accounts.txt`, `available_games.txt` and `game_collection.txt` from the project root.
Accounts: admin = meow_meow_17 (AA, $500.00), full_standard = player_one (FS, $200.00), buy_standard = buyer_bea (BS, $50.00), sell_standard = seller_sam (SS, $1000.00).

## admin/success

Admin meow_meow_17 logs in and then logs out.

## admin/failure

create before login is rejected; login as ghost_user is rejected; after a valid login, a second login is rejected.

## full_standard/success

Full-standard user player_one logs in and then logs out.

## full_standard/failure

addcredit before login is rejected; login as player_two (not a user) is rejected; after a valid login as player_one, a second login is rejected.

## buy_standard/success

Buy-standard user buyer_bea logs in and then logs out.

## buy_standard/failure

buy before login is rejected; login as buyer_be (not a user) is rejected; after a valid login as buyer_bea, a second login is rejected.

## sell_standard/success

Sell-standard user seller_sam logs in and then logs out.

## sell_standard/failure

sell before login is rejected; login as seller_sammy (not a user) is rejected; after a valid login as seller_sam, a second login is rejected.

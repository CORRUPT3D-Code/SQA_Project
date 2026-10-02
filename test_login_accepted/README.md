# test_login_accepted

Login asks for a username and accepts it when it matches an account in the current user accounts file.

Reads `current_user_accounts.txt`, `available_games.txt` and `game_collection.txt` from the project root.
Accounts: admin = meow_meow_17 (AA, $500.00), full_standard = player_one (FS, $200.00), buy_standard = buyer_bea (BS, $50.00), sell_standard = seller_sam (SS, $1000.00).

## admin/success

Admin logs in as meow_meow_17 and then logs out.

## admin/failure

Login as Meow_Meow_17 (wrong case) is rejected because it does not match the accounts file exactly.

## full_standard/success

Full-standard user player_one logs in with the exact username from the accounts file, then logs out.

## full_standard/failure

Login as Player_One (wrong case) is rejected because it does not match the accounts file exactly.

## buy_standard/success

Buy-standard user buyer_bea logs in with the exact username from the accounts file, then logs out.

## buy_standard/failure

Login as Buyer_Bea (wrong case) is rejected because it does not match the accounts file exactly.

## sell_standard/success

Sell-standard user seller_sam logs in with the exact username from the accounts file, then logs out.

## sell_standard/failure

Login as Seller_Sam (wrong case) is rejected because it does not match the accounts file exactly.

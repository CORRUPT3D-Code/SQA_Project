# test_login_accepted

Login asks for a username and accepts it when it matches an account in the current user accounts file.

Reads `current_user_accounts.txt` and `available_games.txt` from the project root.

## success

Admin logs in as meow_meow_17 and then logs out.

## failure

Login as Meow_Meow_17 (wrong case) is rejected because it does not match the accounts file exactly.

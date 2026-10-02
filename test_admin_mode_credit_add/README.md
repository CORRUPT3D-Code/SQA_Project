# test_admin_mode_credit_add

In admin mode, addcredit asks for the amount of credit to add and the account to add it to.

Reads `current_user_accounts.txt` and `available_games.txt` from the project root.

## success

Admin adds $250.00 to player_one: asked for the amount, then the username.

## failure

Admin enters a negative amount (-50.00): rejected before the username is asked for.

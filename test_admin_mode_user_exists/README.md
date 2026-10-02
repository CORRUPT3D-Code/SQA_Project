# test_admin_mode_user_exists

In admin mode, the username entered for addcredit must exist in the system.

Reads `current_user_accounts.txt` and `available_games.txt` from the project root.

## success

Admin adds $50.00 to existing user buyer_bea: accepted.

## failure

Admin adds $50.00 to nobody_here, who does not exist: rejected.

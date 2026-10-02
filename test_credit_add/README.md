# test_credit_add

In standard mode, addcredit asks only for the amount and adds it to the current user.

Reads `current_user_accounts.txt` and `available_games.txt` from the project root.

## success

player_one adds $100.00 to their own account: balance $300.00.

## failure

player_one enters a non-numeric amount (abc): rejected.

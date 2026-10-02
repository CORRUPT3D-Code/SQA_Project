# test_create_rejected

A standard user cannot perform the privileged create transaction.

Reads `current_user_accounts.txt` and `available_games.txt` from the project root.

## success

Admin creates fresh_player (sell-standard): accepted.

## failure

Full-standard user player_one enters create: rejected immediately and nothing is saved for a new user.

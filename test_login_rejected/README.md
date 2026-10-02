# test_login_rejected

Logins and transactions are rejected when invalid: an unknown username, any transaction before login, or a second login while already logged in.

Reads `current_user_accounts.txt` and `available_games.txt` from the project root.

## success

Full-standard user player_one logs in and then logs out.

## failure

create before login is rejected; login as ghost_user is rejected; after a valid login, a second login is rejected.

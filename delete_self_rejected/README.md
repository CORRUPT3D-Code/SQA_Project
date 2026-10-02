# delete_self_rejected

An admin cannot delete the account they are currently logged in as.

Reads `current_user_accounts.txt` and `available_games.txt` from the project root.

## success

Admin deletes a different user, buyer_bea: accepted.

## failure

Admin tries to delete meow_meow_17 (themselves): rejected.

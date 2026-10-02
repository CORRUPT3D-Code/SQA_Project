# delete_user

Admin deletes an existing user who is not the current user; the user's games are cancelled and no further transactions are accepted on them.

Reads `current_user_accounts.txt` and `available_games.txt` from the project root.

## success

Admin deletes seller_sam, then tries to buy seller_sam's Space Raiders: the buy is rejected.

## failure

Admin tries to delete ghost_user, who does not exist: rejected.

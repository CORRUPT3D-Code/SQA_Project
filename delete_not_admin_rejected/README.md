# delete_not_admin_rejected

Someone logged in as a non-admin should not be able to use delete.

Reads `current_user_accounts.txt` and `available_games.txt` from the project root.

## success

Admin deletes player_one: accepted.

## failure

Full-standard user player_one enters delete: rejected immediately, no username prompt.

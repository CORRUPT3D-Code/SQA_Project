# test_create_accepted

An admin creates new users by entering a username and a user type; each is saved to the daily transaction file.

Reads `current_user_accounts.txt` and `available_games.txt` from the project root.

## success

Admin creates new_gamer (full-standard) and fifteen_chars_x (buy-standard, boundary: exactly 15 characters).

## failure

Admin enters invalid create input: a 16-character username, an existing username (player_one), and an invalid user type. All three are rejected.

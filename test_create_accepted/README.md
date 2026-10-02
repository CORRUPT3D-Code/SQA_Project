# test_create_accepted

An admin creates new users by entering a username and a user type; each is saved to the daily transaction file.

Reads `current_user_accounts.txt`, `available_games.txt` and `game_collection.txt` from the project root.
Accounts: admin = meow_meow_17 (AA, $500.00), full_standard = player_one (FS, $200.00), buy_standard = buyer_bea (BS, $50.00), sell_standard = seller_sam (SS, $1000.00).

## admin/success

Admin creates new_gamer (full-standard) and fifteen_chars_x (buy-standard, boundary: exactly 15 characters).

## admin/failure

Admin enters invalid create input: a 16-character username, an existing username (player_one), and an invalid user type. All three are rejected.

## full_standard/success

Full-standard user player_one enters create: rejected immediately with no prompts, and the session continues to a normal logout.

## full_standard/failure

Full-standard user player_one enters create and then types its inputs anyway (new_gamer, full-standard): create is rejected, each extra line is rejected as an unknown command, and nothing is saved.

## buy_standard/success

Buy-standard user buyer_bea enters create: rejected immediately with no prompts, and the session continues to a normal logout.

## buy_standard/failure

Buy-standard user buyer_bea enters create and then types its inputs anyway (new_gamer, full-standard): create is rejected, each extra line is rejected as an unknown command, and nothing is saved.

## sell_standard/success

Sell-standard user seller_sam enters create: rejected immediately with no prompts, and the session continues to a normal logout.

## sell_standard/failure

Sell-standard user seller_sam enters create and then types its inputs anyway (new_gamer, full-standard): create is rejected, each extra line is rejected as an unknown command, and nothing is saved.

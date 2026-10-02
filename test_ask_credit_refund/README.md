# test_ask_credit_refund

Refund asks for the buyer's username, the seller's username and the amount of credit to transfer.

Reads `current_user_accounts.txt` and `available_games.txt` from the project root.

## success

Admin refunds $20.00 from seller_sam to player_one: all three prompts appear.

## failure

Full-standard user player_one enters refund (privileged): rejected and no prompts appear.

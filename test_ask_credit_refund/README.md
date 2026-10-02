# test_ask_credit_refund

Refund asks for the buyer's username, the seller's username and the amount of credit to transfer.

Reads `current_user_accounts.txt`, `available_games.txt` and `game_collection.txt` from the project root.
Accounts: admin = meow_meow_17 (AA, $500.00), full_standard = player_one (FS, $200.00), buy_standard = buyer_bea (BS, $50.00), sell_standard = seller_sam (SS, $1000.00).

## admin/success

Admin refunds $20.00 from seller_sam to player_one: all three prompts appear.

## admin/failure

Admin enters a negative refund amount (-20.00): all three prompts appear, then the refund is rejected.

## full_standard/success

Full-standard user player_one enters refund: rejected, but the session carries on and an allowed addcredit of $10.00 is accepted.

## full_standard/failure

Full-standard user player_one enters refund (privileged): rejected and no prompts appear.

## buy_standard/success

Buy-standard user buyer_bea enters refund: rejected immediately with no prompts, and the session continues to a normal logout.

## buy_standard/failure

Buy-standard user buyer_bea enters refund and then types its inputs anyway (player_one, seller_sam, 20.00): refund is rejected, each extra line is rejected as an unknown command, and nothing is saved.

## sell_standard/success

Sell-standard user seller_sam enters refund: rejected immediately with no prompts, and the session continues to a normal logout.

## sell_standard/failure

Sell-standard user seller_sam enters refund and then types its inputs anyway (player_one, seller_sam, 20.00): refund is rejected, each extra line is rejected as an unknown command, and nothing is saved.

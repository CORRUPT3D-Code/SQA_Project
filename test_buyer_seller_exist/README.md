# test_buyer_seller_exist

Refund requires the buyer and the seller to both be current users.

Reads `current_user_accounts.txt`, `available_games.txt` and `game_collection.txt` from the project root.
Accounts: admin = meow_meow_17 (AA, $500.00), full_standard = player_one (FS, $200.00), buy_standard = buyer_bea (BS, $50.00), sell_standard = seller_sam (SS, $1000.00).

## admin/success

Admin refunds $10.00 from seller_sam to buyer_bea (both exist): accepted.

## admin/failure

Admin refunds to ghost_buyer (does not exist), then from ghost_seller (does not exist): both rejected.

## full_standard/success

Full-standard user player_one enters refund: rejected immediately with no prompts, and the session continues to a normal logout.

## full_standard/failure

Full-standard user player_one enters refund and then types its inputs anyway (buyer_bea, seller_sam, 10.00): refund is rejected, each extra line is rejected as an unknown command, and nothing is saved.

## buy_standard/success

Buy-standard user buyer_bea enters refund: rejected immediately with no prompts, and the session continues to a normal logout.

## buy_standard/failure

Buy-standard user buyer_bea enters refund and then types its inputs anyway (buyer_bea, seller_sam, 10.00): refund is rejected, each extra line is rejected as an unknown command, and nothing is saved.

## sell_standard/success

Sell-standard user seller_sam enters refund: rejected immediately with no prompts, and the session continues to a normal logout.

## sell_standard/failure

Sell-standard user seller_sam enters refund and then types its inputs anyway (buyer_bea, seller_sam, 10.00): refund is rejected, each extra line is rejected as an unknown command, and nothing is saved.

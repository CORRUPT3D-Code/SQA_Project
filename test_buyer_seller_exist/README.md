# test_buyer_seller_exist

Refund requires the buyer and the seller to both be current users.

Reads `current_user_accounts.txt` and `available_games.txt` from the project root.

## success

Admin refunds $10.00 from seller_sam to buyer_bea (both exist): accepted.

## failure

Admin refunds to ghost_buyer (does not exist), then from ghost_seller (does not exist): both rejected.

# test_add_funds

The game's price is added to the seller's wallet.

Reads `current_user_accounts.txt`, `available_games.txt` and `game_collection.txt` from the project root.
Accounts: admin = meow_meow_17 (AA, $500.00), full_standard = player_one (FS, $200.00), buy_standard = buyer_bea (BS, $50.00), sell_standard = seller_sam (SS, $1000.00).

## admin/success

Admin buys Pixel Quest from seller_sam: seller_sam is credited $15.00.

## admin/failure

Admin tries to buy Pixel Quest from buyer_bea, who owns it but is not selling it: no funds move.

## full_standard/success

player_one buys Space Raiders from seller_sam: seller_sam is credited $20.00.

## full_standard/failure

player_one tries to buy Space Raiders from buyer_bea, who is not selling it: no funds are added to anyone.

## buy_standard/success

buyer_bea buys Space Raiders from seller_sam: seller_sam is credited $20.00.

## buy_standard/failure

buyer_bea tries to buy Space Raiders from player_one, who is not selling it: no funds move.

## sell_standard/success

Sell-standard user seller_sam enters buy: rejected immediately with no prompts, and the session continues to a normal logout.

## sell_standard/failure

Sell-standard user seller_sam enters buy and then types its inputs anyway (Space Raiders, seller_sam): buy is rejected, each extra line is rejected as an unknown command, and nothing is saved.

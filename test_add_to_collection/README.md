# test_add_to_collection

The purchased game is added to the user's game collection.

Reads `current_user_accounts.txt`, `available_games.txt` and `game_collection.txt` from the project root.
Accounts: admin = meow_meow_17 (AA, $500.00), full_standard = player_one (FS, $200.00), buy_standard = buyer_bea (BS, $50.00), sell_standard = seller_sam (SS, $1000.00).

## admin/success

Admin buys Space Raiders: it is added to the admin's collection.

## admin/failure

Admin tries to buy Moon Miners, which is not for sale: nothing is added.

## full_standard/success

player_one buys Pixel Quest from seller_sam: it is added to the collection.

## full_standard/failure

player_one tries to buy Moon Miners, which is not for sale: nothing is added to the collection.

## buy_standard/success

buyer_bea buys Dungeon Delve: it is added to her collection.

## buy_standard/failure

buyer_bea tries to buy Pixel Quest, which is already in her collection: it is not added again.

## sell_standard/success

Sell-standard user seller_sam enters buy: rejected immediately with no prompts, and the session continues to a normal logout.

## sell_standard/failure

Sell-standard user seller_sam enters buy and then types its inputs anyway (Pixel Quest, seller_sam): buy is rejected, each extra line is rejected as an unknown command, and nothing is saved.

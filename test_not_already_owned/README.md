# test_not_already_owned

The buyer must not already have a copy of the game in their collection.

Reads `current_user_accounts.txt`, `available_games.txt` and `game_collection.txt` from the project root.
Accounts: admin = meow_meow_17 (AA, $500.00), full_standard = player_one (FS, $200.00), buy_standard = buyer_bea (BS, $50.00), sell_standard = seller_sam (SS, $1000.00).

## admin/success

Admin (who owns only Castle Siege) buys Pixel Quest: accepted.

## admin/failure

Admin tries to buy Castle Siege, which is already in the admin's collection: rejected.

## full_standard/success

player_one (who owns only Titan Wars) buys Pixel Quest: accepted.

## full_standard/failure

player_one tries to buy Titan Wars, which is already in their collection: rejected.

## buy_standard/success

buyer_bea (who owns only Pixel Quest) buys Space Raiders: accepted.

## buy_standard/failure

buyer_bea tries to buy Pixel Quest, which is already in her collection: rejected.

## sell_standard/success

Sell-standard user seller_sam enters buy: rejected immediately with no prompts, and the session continues to a normal logout.

## sell_standard/failure

Sell-standard user seller_sam enters buy and then types its inputs anyway (Pixel Quest, seller_sam): buy is rejected, each extra line is rejected as an unknown command, and nothing is saved.

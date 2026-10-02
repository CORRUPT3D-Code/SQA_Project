# test_deduct_funds

The game's price is deducted from the buyer's wallet.

Reads `current_user_accounts.txt`, `available_games.txt` and `game_collection.txt` from the project root.
Accounts: admin = meow_meow_17 (AA, $500.00), full_standard = player_one (FS, $200.00), buy_standard = buyer_bea (BS, $50.00), sell_standard = seller_sam (SS, $1000.00).

## admin/success

Admin buys Ocean Odyssey ($50.00): balance drops from $500.00 to $450.00.

## admin/failure

Admin tries to buy Ocean Odyssey from ghost_seller, who does not exist: balance stays $500.00.

## full_standard/success

player_one buys Dungeon Delve ($35.50): balance drops from $200.00 to $164.50.

## full_standard/failure

player_one tries to buy Dungeon Delve from ghost_seller, who does not exist: balance stays $200.00.

## buy_standard/success

buyer_bea buys Space Raiders ($20.00): balance drops from $50.00 to $30.00.

## buy_standard/failure

buyer_bea tries to buy Titan Wars ($120.00) with $50.00: rejected and nothing is deducted.

## sell_standard/success

Sell-standard user seller_sam enters buy: rejected immediately with no prompts, and the session continues to a normal logout.

## sell_standard/failure

Sell-standard user seller_sam enters buy and then types its inputs anyway (Ocean Odyssey, seller_sam): buy is rejected, each extra line is rejected as an unknown command, and nothing is saved.

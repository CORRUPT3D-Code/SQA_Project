# test_sufficient_funds

The buyer must have enough credit to pay for the game.

Reads `current_user_accounts.txt`, `available_games.txt` and `game_collection.txt` from the project root.
Accounts: admin = meow_meow_17 (AA, $500.00), full_standard = player_one (FS, $200.00), buy_standard = buyer_bea (BS, $50.00), sell_standard = seller_sam (SS, $1000.00).

## admin/success

Admin ($500.00) buys Titan Wars ($120.00): accepted, balance $380.00.

## admin/failure

Admin ($500.00) tries to buy Dragon Realm ($750.00): rejected for insufficient funds.

## full_standard/success

Boundary: player_one ($200.00) buys Castle Siege for exactly $200.00 and is left with $0.00.

## full_standard/failure

player_one ($200.00) tries to buy Dragon Realm ($750.00): rejected for insufficient funds.

## buy_standard/success

Boundary: buyer_bea ($50.00) buys Ocean Odyssey for exactly $50.00 and is left with $0.00.

## buy_standard/failure

buyer_bea ($50.00) tries to buy Titan Wars ($120.00): rejected for insufficient funds.

## sell_standard/success

Sell-standard user seller_sam enters buy: rejected immediately with no prompts, and the session continues to a normal logout.

## sell_standard/failure

Sell-standard user seller_sam enters buy and then types its inputs anyway (Titan Wars, seller_sam): buy is rejected, each extra line is rejected as an unknown command, and nothing is saved.

# test_valid_game

The game name entered for buy must be an existing game for sale.

Reads `current_user_accounts.txt`, `available_games.txt` and `game_collection.txt` from the project root.
Accounts: admin = meow_meow_17 (AA, $500.00), full_standard = player_one (FS, $200.00), buy_standard = buyer_bea (BS, $50.00), sell_standard = seller_sam (SS, $1000.00).

## admin/success

Admin buys Pixel Quest, which exists: accepted.

## admin/failure

Admin puts Moon Base up for sale, then tries to buy it in the same session: rejected, because a new game cannot be bought until the next session.

## full_standard/success

player_one buys Ocean Odyssey, which exists: accepted.

## full_standard/failure

player_one tries to buy Starfield Quest, which does not exist: rejected.

## buy_standard/success

buyer_bea buys Space Raiders, which exists: accepted.

## buy_standard/failure

buyer_bea tries to buy Space Raider (missing the final s): rejected because no game has that exact name.

## sell_standard/success

Sell-standard user seller_sam enters buy: rejected immediately with no prompts, and the session continues to a normal logout.

## sell_standard/failure

Sell-standard user seller_sam enters buy and then types its inputs anyway (Space Raiders, seller_sam): buy is rejected, each extra line is rejected as an unknown command, and nothing is saved.

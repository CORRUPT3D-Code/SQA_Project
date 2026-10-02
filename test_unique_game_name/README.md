# test_unique_game_name

A game for sale must have a name that no other game already uses.

Reads `current_user_accounts.txt`, `available_games.txt` and `game_collection.txt` from the project root.
Accounts: admin = meow_meow_17 (AA, $500.00), full_standard = player_one (FS, $200.00), buy_standard = buyer_bea (BS, $50.00), sell_standard = seller_sam (SS, $1000.00).

## admin/success

Admin puts Moon Base up for sale, a new name: accepted.

## admin/failure

Admin puts Moon Base up for sale, then tries to sell another game named Moon Base: the second is rejected because names must be unique, including games added this session.

## full_standard/success

player_one sells Star Forge, a new name: accepted.

## full_standard/failure

player_one tries to sell Space Raiders, which seller_sam already sells: rejected.

## buy_standard/success

Buy-standard user buyer_bea enters sell: rejected immediately with no prompts, and the session continues to a normal logout.

## buy_standard/failure

Buy-standard user buyer_bea enters sell and then types its inputs anyway (Star Forge, 25.00): sell is rejected, each extra line is rejected as an unknown command, and nothing is saved.

## sell_standard/success

seller_sam puts Neon Drift up for sale, a new name: accepted.

## sell_standard/failure

seller_sam tries to sell Dungeon Delve, a name he is already selling: rejected.

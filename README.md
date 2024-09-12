# Speed Runs Data Scraping Repository

This repository contains the code to retrieve run data from the Speedrun API. It includes different scripts that scrape accessible information about games, players, and more.

## Files

### `games.ipynb`

This script retrieves all game IDs from the API. The variable `maxSizeAPIv1=200` is used because it is the maximum number of IDs that can be retrieved per API call.

### `games_info.ipynb`

This script uses Beautiful Soup to extract additional information about the games that is not available via the API. The data retrieved includes:

- Number of followers
- Number of runs
- Number of players

### `data.ipynb`

This script identifies the games that represent the median number of players. In this case, it was 519 games. The script uses the API to retrieve the categories, levels, and variables associated with these games.

#### Key Points:

- Categories represent the way the speedrun was completed. For example, if there are 100 coins to collect in a level, the categories could be "run collecting 100 coins, 75 coins, 25 coins, or 0 coins."
- There are two types of categories:
  - Level-based runs
  - Full-game runs
- The script retrieves the best runs for each player, meaning a player cannot have two runs in the same level and category.

### `platforms.ipynb`

This script retrieves the platform names associated with their respective platform IDs.

### `all_players.ipynb`

This script retrieves information associated with each player's ID.

### `obsolate_runs_all_players.ipynb`

Since `data.ipynb` only retrieves the best runs for each player, this script retrieves the runs that were once uploaded but were later surpassed by better times from the same player.

### `joins.ipynb`

This script performs the necessary joins on the obtained CSVs to replace IDs with real names.

## Notes

- The API limits data retrieval to 200 IDs per call, and some additional data scraping is done using Beautiful Soup to gather game-related data not provided by the API.
- Full-game runs and level-based runs are treated as separate categories, and only the best run per player is retained for each game/category combination.


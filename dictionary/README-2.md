# Video Game Speed Run Dataset

This dataset contains information related to video games and speed runs, including game categories, player performance, world records, and forum interactions. Below is the detailed data dictionary explaining each column in the dataset.

## Data Dictionary

| **Column Name**                  | **Description**                                                                                                  |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------|
| `categoryID`                      | ID of the run's category type (e.g., full-game run or level run).                                                |
| `levelID`                         | ID of the game level. If `levelID` is 0, it indicates a full game run and not a specific level.                   |
| `status`                          | Indicates whether the run was verified by the website moderators.                                                |
| `total_seconds`                   | Total run time in seconds, calculated from the aggregate of hours, minutes, and seconds.                         |
| `is_world_record`                 | Boolean indicating whether this run set a world record for the given category-level combination.                  |
| `forum_interaction_run_year`      | Number of interactions the game received on the forum in the year the run was performed.                         |
| `y_baseline_j`                    | The baseline time of the first world record for the game.                                                        |
| `y*_jt`                           | Normalized world record time for game *j* at date *t*.                                                           |
| `Delta_jt`                        | Marginal improvement in world record time: \( \Delta_jt = (y*_jt - y*_{j,t-1}) \).                               |
| `breakthrough_1`                  | Boolean indicating whether \( \Delta_jt \) exceeded a threshold (sigma).                                         |
| `breakthrough_2`                  | Boolean indicating whether \( \Delta_jt \) exceeded twice the threshold (2*sigma).                               |
| `breakthrough_3`                  | Boolean indicating whether \( \Delta_jt \) exceeded three times the threshold (3*sigma).                         |
| `delta_jt`                        | Relative marginal improvement: \( \delta_jt = \frac{(y*_jt - y*_{j,t-1})}{y*_{j,t-1}} \).                       |
| `rel_breakthrough_1`              | Boolean indicating whether the relative improvement \( \delta_jt \) exceeded the threshold (sigma).              |
| `rel_breakthrough_2`              | Boolean indicating whether \( \delta_jt \) exceeded twice the threshold (2*sigma).                               |
| `rel_breakthrough_3`              | Boolean indicating whether \( \delta_jt \) exceeded three times the threshold (3*sigma).                         |
| `favorite_game1`                  | Player’s favorite game at the time of the run.                                                                   |
| `percentage_users_favorite_game1` | Percentage of users of the game (associated with the run) who played their favorite game during that time.        |
| `favorite_game2`                  | Another favorite game of the player.                                                                             |
| `percentage_users_favorite_game2` | Percentage of users playing their second favorite game during that time.                                          |
| `favorite_game3`                  | A third favorite game of the player.                                                                             |
| `percentage_users_favorite_game3` | Percentage of users playing their third favorite game during that time.                                           |
| `favorite_game4`                  | A fourth favorite game of the player.                                                                            |
| `percentage_users_favorite_game4` | Percentage of users playing their fourth favorite game during that time.                                          |
| `mejor_amigo_de_mi_amigo`         | The "best friend" of the player’s favorite game, who is not their best friend.                                    |
| `cat-level_ID`                    | Combined ID representing the category and level of the run.                                                      |
| `runID`                           | ID of the speed run.                                                                                             |
| `gameID`                          | ID of the game the run belongs to.                                                                               |
| `date`                            | Date when the run was completed.                                                                                 |
| `hours`, `minutes`, `seconds`     | Breakdown of the run duration into hours, minutes, and seconds.                                                  |
| `platformID`                      | ID of the platform the run was performed on.                                                                     |
| `playerID`                        | ID of the player who completed the run.                                                                          |
| `speed_run_comment`               | Any comments made by the player about the speed run.                                                             |
| `speed_run_web_link`              | Link to the speed run's webpage.                                                                                 |
| `game_name`                       | Name of the game the run is associated with.                                                                     |
| `game_web_link`                   | Link to the game's webpage.                                                                                      |
| `game_date_released`              | Release date of the game.                                                                                        |
| `game_ruleset`                    | The set of rules that govern the game's speed run categories.                                                    |
| `game_default_time`               | The default time expected for the game.                                                                          |
| `game_platforms`                  | Platforms on which the game can be played.                                                                       |
| `game_num_players`                | Total number of players who have performed runs in this game.                                                    |
| `game_num_runs`                   | Total number of speed runs submitted for the game.                                                               |
| `game_num_followers`              | Total number of followers for the game on the platform.                                                          |
| `category_name`                   | Name of the category in which the speed run was performed.                                                       |
| `category_rules`                  | Rules specific to the category.                                                                                  |
| `category_type`                   | Type of category (e.g., level-based or full-game).                                                               |
| `category_num_players`            | Number of players participating in the category.                                                                 |
| `platform_name`                   | Name of the platform on which the run was performed.                                                             |
| `plataform_date_released`         | Release date of the platform.                                                                                    |
| `level_name`                      | Name of the game level.                                                                                          |
| `level_rules`                     | Rules specific to the level.                                                                                     |
| `years_ago_text`                  | Textual representation of how many years ago the run was performed.                                              |

---

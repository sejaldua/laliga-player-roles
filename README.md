# LaLiga 2025/26 player roles

<a href="https://colab.research.google.com/github/sejaldua/laliga-player-roles/blob/main/notebooks/laliga_archetypes_starter.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

Season-level stats and heatmaps for LaLiga 2025/26 outfield players, prepared for
**clustering players into role archetypes**. Start with the notebook (badge above).
It clones this repo, loads every table and includes a starter clustering pipeline.

## What's in the data

- **Eligible players:** 299. That's outfield players with ≥ 900 league minutes, excluding anyone who played for more than one club during the season.
- **Player pool:** 426 players with ≥ 450 minutes are kept in the long tables, so other thresholds are possible.
- **Season-total stats** (not per-90, to describe roles rather than quality), plus derived stats: npxG, possession-adjusted tackles/interceptions, and minutes-independent style ratios.
- **Season heatmaps:** raw points, a 6×5 zone grid, and summary location features.
- **Per-90 versions,** for ranking players within an archetype.

| File | One row per |
|---|---|
| `model_features.csv` | eligible player: **everything joined; start here** |
| `data_dictionary.csv` | table × column: unit, description, SofaScore source |
| `player_season_eligibility.csv` | pool player: minutes + inclusion rules |
| `players.csv`, `player_positions.csv` | player / player × detailed position |
| `player_season_stats.csv`, `player_season_per90.csv` | pool player: totals / per-90 |
| `heatmap_summary.csv`, `heatmap_zones.csv`, `heatmap_points.csv` | player / player × zone / player × point |
| `player_season_clubs.csv`, `player_transfers.csv` | club spells & transfers (how movers were detected) |
| `teams.csv`, `seasons.csv` | team possession / build settings |

Heatmap coordinates are 0–100. x runs from your own goal (0) to the opponent's goal (100). y = 0 is the **right** touchline and y = 100 the **left**.

## Source

Data collected from [SofaScore](https://www.sofascore.com) for non-commercial, educational use. It is not affiliated with or endorsed by SofaScore. Season 2025/26, LaLiga league matches only, built October 2026.

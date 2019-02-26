# Faulty Node Tests
## Manual Tests
### Test 1

| FAULTY (F) | HEALTHY (H) | REQUIRED H FOR MINING | MINING EXPECTED | MINING ACTUAL | PASSED | TOTAL (F+H) | NOTES |  |
|------------|-------------|-----------------------|-----------------|---------------|--------------------|-------------|-------------------------------------------------------|----------------------------|
| 2 | 4 | 5 | FALSE | TRUE | :x: | 6 | Blocks mined without issues |  |
| 2 | 3 | 5 | FALSE | TRUE | :x: | 5 | Blocks mined with issues: mining slowed to ~20s/block |  |
| 2 | 2 | 5 | FALSE | FALSE | :white_check_mark: | 4 | Blocks not mined |  |
| 2 | 3 | 5 | FALSE | TRUE | :x: | 5 | "Blocks started mining again | but took a while to begin" |
| 3 | 7 | 7 | TRUE | TRUE | :white_check_mark: | 10 | Blocks mining fine |  |
| 3 | 6 | 7 | FALSE | FALSE | :white_check_mark: | 9 | Take down miner 6 - stopped |  |
| 3 | 7 | 7 | TRUE | TRUE | :white_check_mark: | 10 | Bring back miner 6 - started mining again |  |
| 3 | 6 | 7 | FALSE | FALSE | :white_check_mark: | 9 | Take down miner 6 - stopped |  |
| 3 | 5 | 7 | FALSE | FALSE | :white_check_mark: | 8 | Take down miner 5 - stopped |  |
| 3 | 5 | 7 | FALSE | FALSE | :white_check_mark: | 8 | Take down miner 4 - stopped |  |
| 3 | 4 | 7 | FALSE | FALSE | :white_check_mark: | 7 | Take down miner 3 - stopped |  |
| 2 | 4 | 5 | FALSE | FALSE | :white_check_mark: | 6 | Take down faulty 9 |  |
| 2 | 5 | 5 | TRUE | FALSE | :x: | 7 | Spin up a healthy node - did not start mining again |  |
| 2 | 6 | 5 | TRUE | FALSE | :x: | 8 | Spin up a healthy node - did not start mining again |  |
| NEW TEST | - | - | - | - | - | - | - |  |
| 2 | 6 | 5 | TRUE | TRUE | :white_check_mark: | 8 | Initialise nodes with 6 health + 2 faulty |  |
| 2 | 5 | 5 | TRUE | TRUE | :white_check_mark: | 7 | Bring down Node 4 |  |
| 2 | 4 | 5 | FALSE | FALSE | :white_check_mark: | 6 | Bring down Node 3 |  |
| 2 | 5 | 5 | TRUE | FALSE | :x: | 7 | Bring up Node 3 |  |

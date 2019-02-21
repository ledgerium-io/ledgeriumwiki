# Faulty Node Tests
## Manual Tests
### Test 1

| Healty | Faulty | F% | H>2F+1| F(mode) | Notes | MINING EXPECTED | MINING ACTUAL | Test Result |
|--------|--------|------|-----------|---------|--------------------------------------------------------|-----------------|---------------|--------------------|
| 4 | 2 | 0.33 | 5 | 1 | Blocks minted without issues | FALSE | TRUE | :x: |
| 3 | 2 | 0.40 | 5 | 1 | Blocks minted with issues: mining slowed to ~20s/block | FALSE | TRUE | :x: |
| 2 | 2 | 0.50 | 5 | 1 | Blocks not minted | FALSE | FALSE | :white_check_mark: |
| 3 | 2 | 0.40 | 5 | 1 | Blocks started mining again, but took a while to begin | FALSE | TRUE | :x: |
| 7 | 3 | 0.30 | 7 | 1 | Blocks minting fine | TRUE | TRUE | :white_check_mark: |
| 6 | 3 | 0.33 | 7 | 1 | Take down miner 6 - stopped | FALSE | FALSE | :white_check_mark: |
| 7 | 3 | 0.30 | 7 | 1 | Bring back miner 6 - started mining again | TRUE | TRUE | :white_check_mark: |
| 6 | 3 | 0.33 | 7 | 1 | Take down miner 6 - stopped | FALSE | FALSE | :white_check_mark: |
| 5 | 3 | 0.38 | 7 | 1 | Take down miner 5 - stopped | FALSE | FALSE | :white_check_mark: |
| 5 | 3 | 0.38 | 7 | 1 | Take down miner 4 - stopped | FALSE | FALSE | :white_check_mark: |
| 4 | 3 | 0.43 | 7 | 1 | Take down miner 3 - stopped | FALSE | FALSE | :white_check_mark: |
| 4 | 2 | 0.33 | 5 | 1 | Take down faulty 9 | FALSE | FALSE | :white_check_mark: |
| 5 | 2 | 0.29 | 5 | 1 | Spin up a healthy node - did not start mining again | TRUE | FALSE | :x: |
| 6 | 2 | 0.25 | 5 | 1 | Spin up a healthy node - did not start mining again | TRUE | FALSE | :x: |

### Test 2
| Healty | Faulty | F% | H>2F+1| F(mode) | Notes           | MINING EXPECTED | MINING ACTUAL | Test Result |
|--------|--------|------|-----------|-------------------|--------------------------------------------------------|-----------------|---------------|--------------------|
| 6 | 2 | 0.25 | 5 | 1 | INIT | TRUE | TRUE | :white_check_mark: |
| 5 | 2 | 0.29 | 5 | 1 | Bring down Node 4 | TRUE | TRUE | :white_check_mark: |
| 4 | 2 | 0.33 | 5 | 1 | Bring down Node 3 | FALSE | FALSE | :white_check_mark: |
| 5 | 2 | 0.29 | 5 | 1 | Bring up Node 3 | TRUE | FALSE | :x: |

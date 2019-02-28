# Faulty Node Tests
## Manual Tests
### Test 1

| FAULTY (F) | HEALTHY (H) | REQUIRED H FOR MINING | MINING EXPECTED | MINING ACTUAL | PASSED | TOTAL (F+H) | NOTES | 
|------------|-------------|-----------------------|-----------------|---------------|--------------------|-------------|-------------------------------------------------------|
| 2 | 4 | 5 | FALSE | TRUE | :x: | 6 | Blocks mined without issues |  
| 2 | 3 | 5 | FALSE | TRUE | :x: | 5 | Blocks mined with issues: mining slowed to ~20s/block |  
| 2 | 2 | 5 | FALSE | FALSE | :white_check_mark: | 4 | Blocks not mined |  
| 2 | 3 | 5 | FALSE | TRUE | :x: | 5 | "Blocks started mining again but took a while to begin" | 
| 3 | 7 | 7 | TRUE | TRUE | :white_check_mark: | 10 | Blocks mining fine |  
| 3 | 6 | 7 | FALSE | FALSE | :white_check_mark: | 9 | Take down miner 6 - stopped |  
| 3 | 7 | 7 | TRUE | TRUE | :white_check_mark: | 10 | Bring back miner 6 - started mining again |  
| 3 | 6 | 7 | FALSE | FALSE | :white_check_mark: | 9 | Take down miner 6 - stopped |  
| 3 | 5 | 7 | FALSE | FALSE | :white_check_mark: | 8 | Take down miner 5 - stopped |  
| 3 | 5 | 7 | FALSE | FALSE | :white_check_mark: | 8 | Take down miner 4 - stopped |  
| 3 | 4 | 7 | FALSE | FALSE | :white_check_mark: | 7 | Take down miner 3 - stopped |  
| 2 | 4 | 5 | FALSE | FALSE | :white_check_mark: | 6 | Take down faulty 9 |  
| 2 | 5 | 5 | TRUE | FALSE | :x: | 7 | Spin up a healthy node - did not start mining again |  
| 2 | 6 | 5 | TRUE | FALSE | :x: | 8 | Spin up a healthy node - did not start mining again |  


### Test 2

| FAULTY (F) | HEALTHY (H) | REQUIRED H FOR MINING | MINING EXPECTED | MINING ACTUAL | PASSED | TOTAL (F+H) | NOTES |
|------------|-------------|-----------------------|-----------------|---------------|--------------------|-------------|-------------------------------------------------------|
| 2 | 6 | 5 | TRUE | TRUE | :white_check_mark: | 8 | Initialise nodes with 6 health + 2 faulty |  
| 2 | 5 | 5 | TRUE | TRUE | :white_check_mark: | 7 | Bring down Node 4 |  
| 2 | 4 | 5 | FALSE | FALSE | :white_check_mark: | 6 | Bring down Node 3 |  
| 2 | 5 | 5 | TRUE | FALSE | :x: | 7 | Bring up Node 3 |  


### Test 3
| FAULTY (F) | HEALTHY (H) | REQUIRED H FOR MINING | MINING EXPECTED | MINING ACTUAL | PASSED | TOTAL (F+H) | NOTES |
|------------|-------------|-----------------------|-----------------|---------------|--------------------|-------------|-----------------------------------------------------------------------------------------|
| 2 | 5 | 5 | TRUE | TRUE | :white_check_mark: | 7 | Initialise 7 H + 3 F |
| 2 | 4 | 5 | FALSE | FALSE | :white_check_mark: | 6 | Took down 1 H node |
| 2 | 5 | 5 | TRUE | TRUE | :white_check_mark: | 7 | Brought up 1 H |
| 2 | 3 | 5 | FALSE | FALSE | :white_check_mark: | 5 | Took down 2 H node |
| 1 | 4 | 3 | TRUE | FALSE | :x: | 5 | Brought up 1 H - did not start mining after 5 minutes |
| 1 | 4 | 3 | TRUE | FALSE | :x: | 5 | Brought up 1 H - started again after 10 minutes |


### Test 4
| FAULTY (F) | HEALTHY (H) | REQUIRED H FOR MINING | MINING EXPECTED | MINING ACTUAL | PASSED | TOTAL (F+H) | NOTES |
|------------|-------------|-----------------------|-----------------|---------------|--------------------|-------------|-----------------------------------------------------------------------------------------|
| 2 | 5 | 5 | TRUE | TRUE | :white_check_mark: | 7 | Initialise 5 H + 2 F |
| 1 | 3 | 3 | TRUE | FALSE | :x: | 4 | Took down 2 H and 1 F - mining stopped |
| 1 | 4 | 3 | TRUE | FALSE | :x: | 5 | Added another node to try bring it back up. 3 hours later it still did not start mining |

### Test 5
| FAULTY (F) | HEALTHY (H) | REQUIRED H FOR MINING | MINING EXPECTED | MINING ACTUAL | PASSED | TOTAL (F+H) | NOTES |
|------------|-------------|-----------------------|-----------------|---------------|--------------------|-------------|-----------------------------------------------------------------------------------------------------------------------|
| 2 | 7 | 5 | TRUE | TRUE | :white_check_mark: | 9 | Initialised  6H + 2F nodes on a fresh chain |
| 2 | 6 | 5 | TRUE | TRUE | :white_check_mark: | 8 | -1 H node (validator 0) |
| 1 | 6 | 3 | TRUE | TRUE | :white_check_mark: | 7 | -1 F node |
| 2 | 6 | 5 | TRUE | TRUE | :white_check_mark: | 8 | +1 F node |
| 2 | 5 | 5 | TRUE | TRUE | :white_check_mark: | 7 | -1 H node (validator 4) |
| 2 | 4 | 5 | FALSE | FALSE | :white_check_mark: | 6 | -1 H node (validator 5) -> mining stopped |
| 2 | 5 | 5 | TRUE | TRUE | :white_check_mark: | 7 | Let mining stop for a few minutes before bringing +1 H node (validator 5) -> mining started again after a few minutes |
| 2 | 4 | 5 | FALSE | FALSE | :white_check_mark: | 6 | -1 H node - let mining stop for 15 minutes before continuing |
| 2 | 5 | 5 | TRUE | TRUE | :white_check_mark: | 7 | + 1H node ->  15 minutes later still no mining - mining started again after 25 minutes |
| 2 | 4 | 5 | FALSE | FALSE | :white_check_mark: | 6 | -1 H node -> let mining stop for a few minutes before bringing up a H node |
| 2 | 5 | 5 | TRUE | TRUE | :white_check_mark: | 7 | +1 H node -> mining started again after a couple minutes |
| 2 | 4 | 5 | FALSE | FALSE | :white_check_mark: | 6 | -1 H node -> let mining stop for 15 minutes |
| 2 | 5 | 5 | TRUE | TRUE | :white_check_mark: | 7 | +1H  node after mining has been stopped for 15 minutes -> started again after 15 minutes |
| 2 | 4 | 5 | FALSE | FALSE | :white_check_mark: | 6 | -1 H node ->  took down for 2 hours - after about 2.5 hours we got -1 on validator list |
| 2 | 5 | 5 | TRUE | FALSE | :x: | 7 | +1 H node -> a hour later there still no mining being done |
| 2 | 6 | 5 | TRUE | FALSE | :x: | 8 | +1 H node -> no mining for 15 minutes |
| 2 | 7 | 5 | TRUE | FALSE | :x: | 9 | +1 H node -> mining never restarted |

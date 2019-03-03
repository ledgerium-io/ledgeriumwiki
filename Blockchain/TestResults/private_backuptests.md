### Test 1

| FAULTY (F) | HEALTHY (H) | REQUIRED H FOR MINING | MINING EXPECTED | MINING ACTUAL | PASSED | TOTAL (F+H) | NOTES |
|------------|-------------|-----------------------|-----------------|---------------|--------------------|-------------|-------------------------------------------------------|
| 2 | 6 | 5 | TRUE | TRUE | :white_check_mark: | 8 | Initialise nodes with 6 health + 2 faulty |  
| 2 | 5 | 5 | TRUE | TRUE | :white_check_mark: | 7 | Bring down Node 4 |  
| 2 | 4 | 5 | FALSE | FALSE | :white_check_mark: | 6 | Bring down Node 3 |  
| 2 | 5 | 5 | TRUE | FALSE | :x: | 7 | Bring up Node 3 |  


### Test 2
| FAULTY (F) | HEALTHY (H) | REQUIRED H FOR MINING | MINING EXPECTED | MINING ACTUAL | PASSED | TOTAL (F+H) | NOTES |
|------------|-------------|-----------------------|-----------------|---------------|--------------------|-------------|-----------------------------------------------------------------------------------------|
| 2 | 5 | 5 | TRUE | TRUE | :white_check_mark: | 7 | Initialise 7 H + 3 F |
| 2 | 4 | 5 | FALSE | FALSE | :white_check_mark: | 6 | Took down 1 H node |
| 2 | 5 | 5 | TRUE | TRUE | :white_check_mark: | 7 | Brought up 1 H |
| 2 | 3 | 5 | FALSE | FALSE | :white_check_mark: | 5 | Took down 2 H node |
| 1 | 4 | 3 | TRUE | FALSE | :x: | 5 | Brought up 1 H - did not start mining after 5 minutes |
| 1 | 4 | 3 | TRUE | FALSE | :x: | 5 | Brought up 1 H - started again after 10 minutes |


### Test 3
| FAULTY (F) | HEALTHY (H) | REQUIRED H FOR MINING | MINING EXPECTED | MINING ACTUAL | PASSED | TOTAL (F+H) | NOTES |
|------------|-------------|-----------------------|-----------------|---------------|--------------------|-------------|-----------------------------------------------------------------------------------------|
| 2 | 5 | 5 | TRUE | TRUE | :white_check_mark: | 7 | Initialise 5 H + 2 F |
| 1 | 3 | 3 | TRUE | FALSE | :x: | 4 | Took down 2 H and 1 F - mining stopped |
| 1 | 4 | 3 | TRUE | FALSE | :x: | 5 | Added another node to try bring it back up. 3 hours later it still did not start mining |

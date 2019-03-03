| FAULTY (F) | HEALTHY (H) | REQUIRED H FOR MINING (2F+1) | MINING EXPECTED | MINING ACTUAL | PASSED | TOTAL (F+H) | NOTES |
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

# Chapter-3: Storage and Retrieval

## Data Structures that power your database

#### Simplest DB
```bash
#!/bin/bash

db_set() {
    echo "$1,$2" >> database
}

db_get() {
   grep "^$1," database | sed -e "s/^$1,//" | tail -n 1
}
```

1. The above script uses a log file (i.e. database) as a database.
2. The set opeartion simply append the new key value (comma separate) in the log file. Hence, the get operation 
3. Most databases work in a similar fashion.



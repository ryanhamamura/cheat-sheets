## `zpool history <pool-name>`
Useful for checking the logs of everything that has happened with the pool. For 
example, `zpool history <pool-name> | grep create | grep zpool` will return the
command that TrueNAS actually executes when creating a pool through the GUI. 



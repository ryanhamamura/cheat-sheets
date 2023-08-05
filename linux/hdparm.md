# `hdparm`
`hdparm` is a SATA/PATA/SAS command line interface.
[hdparm man page](https://linux.die.net/man/8/hdparm)

### Usage
```bash
hdparm [flags] [device] ..
```
When no flags are give, *-acdgkmur* is assumed. 

#### `-C`
`-C`: Check the current IDE power mode status, which will be one of the following:
- *unknown*
- *active/idle* (normal operation)
- *standby* (low power mode, drive has spun down)
- *sleeping* (lowest power mode, drive is completely shutdown)

The `-S`, `-y`, `-Y`, `-Z` flags can be used to manipulate the IDE power modes. 

#### `-S`
Put the drive into idle (low-power) mode, and also set the standby (spindown) timeout for the drive. A value of zero means "timeouts are disabled." Values from `1` to `240` specify multiples of 5 seconds, yielding timeouts from 5 seconds to 20 minutes. Values from `241` to `251` specify from 1 to 11 units of 30 minutes, yielding timeouts from 30 minutes to 5.5 hours. A value of `252` signifies a timeout of 21 minutes. A value of `253` sets a vendor-defined timeout period between 8 and 12 hours, and the value `254` is reserved. `255` is interpreted as 21 minutes plus 15 seconds. Some older drives may have very different interpretations of these values. 

#### `-y`
Force an IDE drive to immediately enter the lower power consumption `standby` mode, usually causing it to spin down. The current power mode status can be checked using the `-C` flag. 

#### `-Y`
Force an IDE drive to immediately enter the lowest power consumption `sleep` mode, causing it to shutdown completely. A hard or soft reset is requred before the drive can be accessed again (the Linux IDE driver will automatically handle issuing a reset if/when needed). The current power mode status can be checked using the `-C` flag. 

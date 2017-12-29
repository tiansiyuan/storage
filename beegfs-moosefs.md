MooseFS and BeeGFS don't really seem to be in the same category of filesystem though.

BeeGFS comes from the HPC world where it is all about performance, while MooseFS seems more focused on high reliability even in the face of entire machines coming and going.

BeeGFS stores files striped over multiple machines and can use infiniband natively which gives us a system where bandwidth to individual files can reach a bit over 1GB/s (best case) and aggregated bandwidth can reach 30GB/s from a very mixed and unoptimized bioinformatics workload, a lot more when just testing the raw bandwidth.

Since BeeGFS uses an underlying filesystem on each storage target you can of course run raid, zfs or whatever it takes to make you comfortable that the individual storage targets aren't going to be lost - which is what it takes for data to be unavailable.

If you want some extra reliability in BeeGFS it also supports mirroring so you only lose data if you fully lose two storage targets. We can't really afford to run with full mirroring for our 3PB though.


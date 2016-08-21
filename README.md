# configs
configuration files

# cascade zfs settings
``` bash
$ sudo zpool create pool raidz /dev/sda /dev/sdb /dev/sdc /dev/sdd /dev/sde
$ sudo zfs create pool/movies
```

Fixing OS drive crash:
You can run `zpool import` with no arguments, and it will identify the available pools for you.

Asssuming the devices from the old testpool are still there, you will see the "old" testpool, and alongside it a GUID for the pool.

Once you have that pools GUID, you can do `zpool import $id oldtestpool`. After the pool is imported, you can change the mountpoints so they don't overlap with the new testpool's mountpoints.

# configs
configuration files

# cascade zfs settings
sudo zpool create pool raidz /dev/sda /dev/sdb /dev/sdc /dev/sdd /dev/sde
sudo zfs create pool/movies

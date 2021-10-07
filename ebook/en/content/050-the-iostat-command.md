# The `iostat` command

---

The `iostat` command is used for monitoring system `I/O` (input/output) device loading by observing the time the devices are active in relation to their average transfer rates. The `iostat` command generates reports that can be used to change system configuration to better balance the `I/O` load between physical disks.

  The `iostat` is being included in `sysstat` package. If you don’t have it, you need to install first. Command to install on different Distros:

1. **On RedHat / CentOS / Fedora**

  ```
  yum install sysstat
  ```

2. **On Debian / Ubuntu / Linux Mint**

  ```
  apt-get install sysstat
  ```

## Example : 
1. To display information about CPU usage, and I/O statistics for every partition on the system 

```bash
iostat
```

2. To see those details in a more readable format, issue the command iostat -m, which will display the statistics in MB (instead of KB)

```bash
iostat -m
```


# Syntax:
```
iostat [-OPTION] 
```


**Additional Flags and their Functionalities:**
|Short Flag	|Description|
|---|---|
|-c	| Display the CPU utilization report.|
|-d | Display the device utilization report.|
|-h | Make the NFS report displayed by option -n easier to read by a human.|
|-k | Display statistics in kilobytes per second instead of blocks per second. Data displayed are valid only with kernels 2.4 and later.|
|-m | Display statistics in megabytes per second instead of blocks or kilobytes per second. Data displayed are valid only with kernels 2.4 and later.|
|-N | Display the registered device mapper names for any device mapper devices. Useful for viewing LVM2 statistics.|
|-n | Display the network filesystem (NFS) report. This option works only with kernel 2.6.17 and later.|
|-p [ { device [,...] or ALL } ]|The -p option displays statistics for block devices and all their partitions that are used by the system. If a device name is entered on the command line, then statistics for it and all its partitions are displayed. Last, the ALL keyword indicates that statistics have to be displayed for all the block devices and partitions defined by the system, including those that have never been used. Note that this option works only with post 2.5 kernels.|
|-t | Print the time for each report displayed. The timestamp format may depend on the value of the S_TIME_FORMAT environment variable (see below).|
|-V | Print version number then exit.|
|-x | Display extended statistics. This option works with post 2.5 kernels since it needs /proc/diskstats file or a mounted sysfs to get the statistics. This option may also work with older kernels (e.g. 2.4) only if extended statistics are available in /proc/partitions (the kernel needs to be patched for that).|
|-z | Tell iostat to omit output for any devices for which there was no activity during the sample period.|



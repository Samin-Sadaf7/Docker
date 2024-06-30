# Docker
This program can be used like this, to run /misc/img/bin/sh in /misc/img as root:

$ sudo ./contained -m ~/misc/busybox-img/ -u 0 -c /bin/sh
=> validating Linux version...4.7.10.201610222037-1-grsec on x86_64.
=> setting cgroups...memory...cpu...pids...blkio...done.
=> setting rlimit...done.
=> remounting everything with MS_PRIVATE...remounted.
=> making a temp directory and a bind mount there...done.
=> pivoting root...done.
=> unmounting /oldroot.oQ5jOY...done.
=> trying a user namespace...writing /proc/32627/uid_map...writing /proc/32627/gid_map...done.
=> switching to uid 0 / gid 0...done.
=> dropping capabilities...bounding...inheritable...done.
=> filtering syscalls...done.
/ # whoami
root
/ # hostname
05fe5c-three-of-pentacles
/ # exit
=> cleaning cgroups...done.

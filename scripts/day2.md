kishore@DESKTOP-36JK8EO:~$ cd
kishore@DESKTOP-36JK8EO:~$ mkdir demo
kishore@DESKTOP-36JK8EO:~$ ls
data  data.log  demo
kishore@DESKTOP-36JK8EO:~$ mkdir -p abc/demo/test
kishore@DESKTOP-36JK8EO:~$ cd abc/
kishore@DESKTOP-36JK8EO:~/abc$ pwd
/home/kishore/abc
kishore@DESKTOP-36JK8EO:~/abc$ ls
demo
kishore@DESKTOP-36JK8EO:~/abc$ pwd
/home/kishore/abc
kishore@DESKTOP-36JK8EO:~/abc$ cd demo/
kishore@DESKTOP-36JK8EO:~/abc/demo$ ls
test
kishore@DESKTOP-36JK8EO:~/abc/demo$ cd test/
kishore@DESKTOP-36JK8EO:~/abc/demo/test$ pwd
/home/kishore/abc/demo/test
kishore@DESKTOP-36JK8EO:~/abc/demo/test$ cd
kishore@DESKTOP-36JK8EO:~$ pwd
/home/kishore
kishore@DESKTOP-36JK8EO:~$ ls
abc  data  data.log  demo
kishore@DESKTOP-36JK8EO:~$ cd abc/
kishore@DESKTOP-36JK8EO:~/abc$ cd demo
kishore@DESKTOP-36JK8EO:~/abc/demo$ cd test
kishore@DESKTOP-36JK8EO:~/abc/demo/test$ cd
kishore@DESKTOP-36JK8EO:~$ cd abc/demo/tst
-bash: cd: abc/demo/tst: No such file or directory
kishore@DESKTOP-36JK8EO:~$ cd abc/demo/test
kishore@DESKTOP-36JK8EO:~/abc/demo/test$ cd ..
kishore@DESKTOP-36JK8EO:~/abc/demo$
kishore@DESKTOP-36JK8EO:~/abc/demo$ pwd
/home/kishore/abc/demo
kishore@DESKTOP-36JK8EO:~/abc/demo$ cd ..
kishore@DESKTOP-36JK8EO:~/abc$ cd abc/demo/test
-bash: cd: abc/demo/test: No such file or directory
kishore@DESKTOP-36JK8EO:~/abc$ cd
kishore@DESKTOP-36JK8EO:~$ cd abc/demo/test
kishore@DESKTOP-36JK8EO:~/abc/demo/test$ cd ../..
kishore@DESKTOP-36JK8EO:~/abc$ cd
kishore@DESKTOP-36JK8EO:~$ cd abc/demo/test
kishore@DESKTOP-36JK8EO:~/abc/demo/test$ cd
kishore@DESKTOP-36JK8EO:~$ cd -
/home/kishore/abc/demo/test
kishore@DESKTOP-36JK8EO:~/abc/demo/test$ touch test.txt
kishore@DESKTOP-36JK8EO:~/abc/demo/test$ pwd
/home/kishore/abc/demo/test
kishore@DESKTOP-36JK8EO:~/abc/demo/test$ cd
kishore@DESKTOP-36JK8EO:~$ cat /abc/test/demo/test
cat: /abc/test/demo/test: No such file or directory
kishore@DESKTOP-36JK8EO:~$ cat abc/demo/test/test.txt
kishore@DESKTOP-36JK8EO:~$ ls -lstr
total 16
4 drwxr-xr-x 2 kishore kishore 4096 Jun 22 04:44 data
4 drwxr-xr-x 2 kishore kishore 4096 Jun 22 04:50 data.log
4 drwxr-xr-x 2 kishore kishore 4096 Jun 22 04:51 demo
4 drwxr-xr-x 3 kishore kishore 4096 Jun 22 04:55 abc
kishore@DESKTOP-36JK8EO:~$ ls -a
.  ..  .bash_history  .bash_logout  .bashrc  .cache  .hello.txt.swp  .landscape  .motd_shown  .profile  .vim  .viminfo  abc  data  data.log  demo
kishore@DESKTOP-36JK8EO:~$
kishore@DESKTOP-36JK8EO:~$ vi .bashrc
kishore@DESKTOP-36JK8EO:~$
kishore@DESKTOP-36JK8EO:~$
kishore@DESKTOP-36JK8EO:~$ ls *.py
ls: cannot access '*.py': No such file or directory
kishore@DESKTOP-36JK8EO:~$ ls *.txt
ls: cannot access '*.txt': No such file or directory
kishore@DESKTOP-36JK8EO:~$ ls test*
ls: cannot access 'test*': No such file or directory
kishore@DESKTOP-36JK8EO:~$ pwd
/home/kishore
kishore@DESKTOP-36JK8EO:~$ mkdir link
kishore@DESKTOP-36JK8EO:~$ cd link/
kishore@DESKTOP-36JK8EO:~/link$
kishore@DESKTOP-36JK8EO:~/link$ pwd
/home/kishore/link
kishore@DESKTOP-36JK8EO:~/link$ echo "Kishorelytics" >> orginal.txt
kishore@DESKTOP-36JK8EO:~/link$ ls
orginal.txt
kishore@DESKTOP-36JK8EO:~/link$ cat original.txt
cat: original.txt: No such file or directory
kishore@DESKTOP-36JK8EO:~/link$ cat orginal.txt
Kishorelytics
kishore@DESKTOP-36JK8EO:~/link$ ls -lstr
total 4
4 -rw-r--r-- 1 kishore kishore 14 Jun 22 05:47 orginal.txt
kishore@DESKTOP-36JK8EO:~/link$
kishore@DESKTOP-36JK8EO:~/link$ ln orginal.txt team2_data.txt
kishore@DESKTOP-36JK8EO:~/link$ cat team2_data.txt
Kishorelytics
kishore@DESKTOP-36JK8EO:~/link$ cat orginal.txt
Kishorelytics
kishore@DESKTOP-36JK8EO:~/link$ ls -lstr
total 8
4 -rw-r--r-- 2 kishore kishore 14 Jun 22 05:47 team2_data.txt
4 -rw-r--r-- 2 kishore kishore 14 Jun 22 05:47 orginal.txt
kishore@DESKTOP-36JK8EO:~/link$ echo "last" >> orginal.txt
kishore@DESKTOP-36JK8EO:~/link$ cat orginal.txt
Kishorelytics
last
kishore@DESKTOP-36JK8EO:~/link$ cat team2_data.txt
Kishorelytics
last
kishore@DESKTOP-36JK8EO:~/link$ ls -lstr
total 8
4 -rw-r--r-- 2 kishore kishore 19 Jun 22 06:01 team2_data.txt
4 -rw-r--r-- 2 kishore kishore 19 Jun 22 06:01 orginal.txt
kishore@DESKTOP-36JK8EO:~/link$ rm orginal.txt
kishore@DESKTOP-36JK8EO:~/link$ cat team2_data.txt
Kishorelytics
last
kishore@DESKTOP-36JK8EO:~/link$ rm team2_data.txt
kishore@DESKTOP-36JK8EO:~/link$ echo "softlink" >> original.txt
kishore@DESKTOP-36JK8EO:~/link$ cat orginal.txt
cat: orginal.txt: No such file or directory
kishore@DESKTOP-36JK8EO:~/link$ cat original.txt
softlink
kishore@DESKTOP-36JK8EO:~/link$ ln -s original.txt new_data.txt
kishore@DESKTOP-36JK8EO:~/link$ ls -lstr
total 4
4 -rw-r--r-- 1 kishore kishore  9 Jun 22 06:08 original.txt
0 lrwxrwxrwx 1 kishore kishore 12 Jun 22 06:08 new_data.txt -> original.txt
kishore@DESKTOP-36JK8EO:~/link$ rm orginal.txt
rm: cannot remove 'orginal.txt': No such file or directory
kishore@DESKTOP-36JK8EO:~/link$ rm original.txt
kishore@DESKTOP-36JK8EO:~/link$ cat new_data.txt
cat: new_data.txt: No such file or directory
kishore@DESKTOP-36JK8EO:~/link$ cd abc/demo/test
-bash: cd: abc/demo/test: No such file or directory
kishore@DESKTOP-36JK8EO:~/link$ pwd
/home/kishore/link
kishore@DESKTOP-36JK8EO:~/link$ cd abc/demo/test
-bash: cd: abc/demo/test: No such file or directory
kishore@DESKTOP-36JK8EO:~/link$ cd
kishore@DESKTOP-36JK8EO:~$ cd abc/demo/test
kishore@DESKTOP-36JK8EO:~/abc/demo/test$ ld
ld: no input files
kishore@DESKTOP-36JK8EO:~/abc/demo/test$ ls
test.txt
kishore@DESKTOP-36JK8EO:~/abc/demo/test$
kishore@DESKTOP-36JK8EO:~/abc/demo/test$ cd
kishore@DESKTOP-36JK8EO:~$ alias kishorelytics="cd /home/kishore/abc/demo/test"
kishore@DESKTOP-36JK8EO:~$ kishorelytics
kishore@DESKTOP-36JK8EO:~/abc/demo/test$


To run a command as administrator (user "root"), use "sudo <command>".
See "man sudo_root" for details.

kishore@DESKTOP-36JK8EO:~$ pwd
/home/kishore
kishore@DESKTOP-36JK8EO:~$ top
top - 12:20:40 up 9 min,  1 user,  load average: 0.00, 0.01, 0.00
Tasks:  23 total,   1 running,  22 sleeping,   0 stopped,   0 zombie
%Cpu(s):  0.0 us,  2.2 sy,  0.0 ni, 97.8 id,  0.0 wa,  0.0 hi,  0.0 si,  0.0 st
MiB Mem :   5879.3 total,   5230.2 free,    424.2 used,    366.1 buff/cache
MiB Swap:   2048.0 total,   2048.0 free,      0.0 used.   5455.1 avail Mem

    PID USER      PR  NI    VIRT    RES    SHR S  %CPU  %MEM     TIME+ COMMAND
      1 root      20   0   21756  12620   9420 S   0.0   0.2   0:02.08 systemd
      2 root      20   0    3060   1664   1664 S   0.0   0.0   0:00.04 init-systemd(Ub
      8 root      20   0    3076   2032   1792 S   0.0   0.0   0:00.00 init
     66 root      19  -1   50352  15292  14396 S   0.0   0.3   0:00.56 systemd-journal
    119 root      20   0   25264   6400   4864 S   0.0   0.1   0:00.39 systemd-udevd
    128 systemd+  20   0   21452  12416  10368 S   0.0   0.2   0:00.42 systemd-resolve
    129 systemd+  20   0   91020   7424   6656 S   0.0   0.1   0:00.15 systemd-timesyn
    180 root      20   0    4236   2432   2304 S   0.0   0.0   0:00.01 cron
    184 message+  20   0    9588   4992   4480 S   0.0   0.1   0:00.23 dbus-daemon
    193 root      20   0   17960   8448   7552 S   0.0   0.1   0:00.31 systemd-logind
    195 root      20   0 1755840  13440  11520 S   0.0   0.2   0:00.43 wsl-pro-service
    198 syslog    20   0  222508   5376   4352 S   0.0   0.1   0:00.27 rsyslogd
    201 root      20   0    3160   1920   1792 S   0.0   0.0   0:00.01 agetty
    208 root      20   0    3116   1792   1664 S   0.0   0.0   0:00.00 agetty
    223 root      20   0  107012  22272  13184 S   0.0   0.4   0:00.45 unattended-upgr
    342 root      20   0    3064    896    896 S   0.0   0.0   0:00.00 SessionLeader
    344 root      20   0    3080   1024   1024 S   0.0   0.0   0:00.00 Relay(348)
    348 kishore   20   0    6072   5248   3584 S   0.0   0.1   0:00.10 bash
    349 root      20   0    6692   4224   3584 S   0.0   0.1   0:00.03 login
    403 kishore   20   0   20304  11008   9088 S   0.0   0.2   0:00.33 systemd
    404 kishore   20   0   21144   3516   1792 S   0.0   0.1   0:00.00 (sd-pam)
    417 kishore   20   0    6056   4864   3456 S   0.0   0.1   0:00.06 bash
    520 kishore   20   0    9312   5248   3072 R   0.0   0.1   0:00.01 top




















[1]+  Stopped                 top
kishore@DESKTOP-36JK8EO:~$ ps
    PID TTY          TIME CMD
    348 pts/0    00:00:00 bash
    520 pts/0    00:00:00 top
    525 pts/0    00:00:00 ps
kishore@DESKTOP-36JK8EO:~$ ps -aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.2  0.2  21756 12620 ?        Ss   12:10   0:02 /sbin/init
root           2  0.0  0.0   3060  1664 ?        Sl   12:10   0:00 /init
root           8  0.0  0.0   3076  2032 ?        Sl   12:10   0:00 plan9 --control-socket 7 --log-level 4 --server-fd 8 --pipe-fd 10 --log-truncate
root          66  0.0  0.2  50352 15292 ?        S<s  12:10   0:00 /usr/lib/systemd/systemd-journald
root         119  0.0  0.1  25264  6400 ?        Ss   12:10   0:00 /usr/lib/systemd/systemd-udevd
systemd+     128  0.0  0.2  21452 12416 ?        Ss   12:10   0:00 /usr/lib/systemd/systemd-resolved
systemd+     129  0.0  0.1  91020  7424 ?        Ssl  12:10   0:00 /usr/lib/systemd/systemd-timesyncd
root         180  0.0  0.0   4236  2432 ?        Ss   12:10   0:00 /usr/sbin/cron -f -P
message+     184  0.0  0.0   9588  4992 ?        Ss   12:10   0:00 @dbus-daemon --system --address=systemd: --nofork --nopidfile --systemd-activation --syslog-only
root         193  0.0  0.1  17960  8448 ?        Ss   12:10   0:00 /usr/lib/systemd/systemd-logind
root         195  0.0  0.2 1755840 13440 ?       Ssl  12:10   0:00 /usr/libexec/wsl-pro-service -vv
syslog       198  0.0  0.0 222508  5376 ?        Ssl  12:10   0:00 /usr/sbin/rsyslogd -n -iNONE
root         201  0.0  0.0   3160  1920 hvc0     Ss+  12:10   0:00 /sbin/agetty -o -p -- \u --noclear --keep-baud - 115200,38400,9600 vt220
root         208  0.0  0.0   3116  1792 tty1     Ss+  12:10   0:00 /sbin/agetty -o -p -- \u --noclear - linux
root         223  0.0  0.3 107012 22272 ?        Ssl  12:10   0:00 /usr/bin/python3 /usr/share/unattended-upgrades/unattended-upgrade-shutdown --wait-for-signal
root         342  0.0  0.0   3064   896 ?        Ss   12:11   0:00 /init
root         344  0.0  0.0   3080  1024 ?        S    12:11   0:00 /init
kishore      348  0.0  0.0   6072  5248 pts/0    Ss   12:11   0:00 -bash
root         349  0.0  0.0   6692  4224 pts/1    Ss   12:11   0:00 /bin/login -f
kishore      403  0.0  0.1  20304 11008 ?        Ss   12:11   0:00 /usr/lib/systemd/systemd --user
kishore      404  0.0  0.0  21144  3516 ?        S    12:11   0:00 (sd-pam)
kishore      417  0.0  0.0   6056  4864 pts/1    S+   12:11   0:00 -bash
kishore      520  0.0  0.0   9312  5504 pts/0    T    12:20   0:00 top
kishore      530  0.0  0.0   9580  4864 pts/0    R+   12:24   0:00 ps -aux
kishore@DESKTOP-36JK8EO:~$
kishore@DESKTOP-36JK8EO:~$ df -h
Filesystem      Size  Used Avail Use% Mounted on
none            2.9G     0  2.9G   0% /usr/lib/modules/6.6.87.1-microsoft-standard-WSL2
none            2.9G  4.0K  2.9G   1% /mnt/wsl
drivers         184G  103G   82G  56% /usr/lib/wsl/drivers
/dev/sdd       1007G  1.3G  955G   1% /
none            2.9G   72K  2.9G   1% /mnt/wslg
none            2.9G     0  2.9G   0% /usr/lib/wsl/lib
rootfs          2.9G  2.7M  2.9G   1% /init
none            2.9G  476K  2.9G   1% /run
none            2.9G     0  2.9G   0% /run/lock
none            2.9G     0  2.9G   0% /run/shm
none            2.9G   76K  2.9G   1% /mnt/wslg/versions.txt
none            2.9G   76K  2.9G   1% /mnt/wslg/doc
C:\             184G  103G   82G  56% /mnt/c
E:\             196G  1.8G  194G   1% /mnt/e
F:\              98G   96M   98G   1% /mnt/f
tmpfs           2.9G   16K  2.9G   1% /run/user/1000
kishore@DESKTOP-36JK8EO:~$ du sh
du: cannot access 'sh': No such file or directory
kishore@DESKTOP-36JK8EO:~$ du -sh
104K    .
kishore@DESKTOP-36JK8EO:~$ ls -lstr
total 20
4 drwxr-xr-x 2 kishore kishore 4096 Jun 22 04:44 data
4 drwxr-xr-x 2 kishore kishore 4096 Jun 22 04:50 data.log
4 drwxr-xr-x 2 kishore kishore 4096 Jun 22 04:51 demo
4 drwxr-xr-x 3 kishore kishore 4096 Jun 22 04:55 abc
4 drwxr-xr-x 2 kishore kishore 4096 Jun 22 06:12 link
kishore@DESKTOP-36JK8EO:~$ sudo apt-get install zip
[sudo] password for kishore:
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following additional packages will be installed:
  unzip
The following NEW packages will be installed:
  unzip zip
0 upgraded, 2 newly installed, 0 to remove and 0 not upgraded.
Need to get 350 kB of archives.
After this operation, 933 kB of additional disk space will be used.
Do you want to continue? [Y/n] y
Get:1 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 unzip amd64 6.0-28ubuntu4.1 [174 kB]
Get:2 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 zip amd64 3.0-13ubuntu0.2 [176 kB]
Fetched 350 kB in 12s (28.5 kB/s)
Selecting previously unselected package unzip.
(Reading database ... 40768 files and directories currently installed.)
Preparing to unpack .../unzip_6.0-28ubuntu4.1_amd64.deb ...
Unpacking unzip (6.0-28ubuntu4.1) ...
Selecting previously unselected package zip.
Preparing to unpack .../zip_3.0-13ubuntu0.2_amd64.deb ...
Unpacking zip (3.0-13ubuntu0.2) ...
Setting up unzip (6.0-28ubuntu4.1) ...
Setting up zip (3.0-13ubuntu0.2) ...
Processing triggers for man-db (2.12.0-4build2) ...
kishore@DESKTOP-36JK8EO:~$ free -m
               total        used        free      shared  buff/cache   available
Mem:            5879         414        5483           3         113        5464
Swap:           2048           0        2048
kishore@DESKTOP-36JK8EO:~$ free -g
               total        used        free      shared  buff/cache   available
Mem:               5           0           5           0           0           5
Swap:              2           0           2
kishore@DESKTOP-36JK8EO:~$ vi sample.txt
kishore@DESKTOP-36JK8EO:~$ cat sample.txt
Linux is powerful
Kishorelytics
Subscrie it!
I am damn sure I will get the job with good lpa Murugan definitily give me because I will trust murugan I dont have any doubts with murugan...
So he will definitely give whatever i want ..

kishore@DESKTOP-36JK8EO:~$ wc sample.txt
  6  43 235 sample.txt
kishore@DESKTOP-36JK8EO:~$ ws -c
ws: command not found
kishore@DESKTOP-36JK8EO:~$ ws -c sample.txt
ws: command not found
kishore@DESKTOP-36JK8EO:~$ wc -c sample.txt

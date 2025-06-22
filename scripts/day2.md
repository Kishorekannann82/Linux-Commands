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

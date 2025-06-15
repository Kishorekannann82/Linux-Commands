kishore@DESKTOP-36JK8EO:~$ pwd
/home/kishore
kishore@DESKTOP-36JK8EO:~$ uname -a
Linux DESKTOP-36JK8EO 6.6.87.1-microsoft-standard-WSL2 #1 SMP PREEMPT_DYNAMIC Mon Apr 21 17:08:54 UTC 2025 x86_64 x86_64 x86_64 GNU/Linux
kishore@DESKTOP-36JK8EO:~$ whoami
kishore
kishore@DESKTOP-36JK8EO:~$clear
kishore@DESKTOP-36JK8EO:~$ history
    1  pwd
    2  0868
    3  exit
    4  pwd
    5  uname -a
    6  whoami
    7  clear
    8  history
kishore@DESKTOP-36JK8EO:~/data$ vi hello.txt
kishore@DESKTOP-36JK8EO:~/data$ ls
hello.txt
kishore@DESKTOP-36JK8EO:~/data$ pwd
/home/kishore/data
kishore@DESKTOP-36JK8EO:~/data$ vi hello.txt
kishore@DESKTOP-36JK8EO:~/data$ vi hello.txt
kishore@DESKTOP-36JK8EO:~/data$ sudo apt-get install vim
[sudo] password for kishore:
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
vim is already the newest version (2:9.1.0016-1ubuntu7.6).
vim set to manually installed.
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
kishore@DESKTOP-36JK8EO:~/data$ ls
hello.txt
kishore@DESKTOP-36JK8EO:~/data$ cat hello.txt new_hello.txt
asaishishidh
cat: new_hello.txt: No such file or directory
kishore@DESKTOP-36JK8EO:~/data$ cp hello.txt new_hello.txt
kishore@DESKTOP-36JK8EO:~/data$ ls
hello.txt  new_hello.txt
kishore@DESKTOP-36JK8EO:~/data$ cat new_hello.txt
asaishishidh
kishore@DESKTOP-36JK8EO:~/data$ mv hello.txt demo.txt
kishore@DESKTOP-36JK8EO:~/data$ ls
demo.txt  new_hello.txt
kishore@DESKTOP-36JK8EO:~/data$ cat demo.txt >> rfile.txt
kishore@DESKTOP-36JK8EO:~/data$ ls
demo.txt  new_hello.txt  rfile.txt
kishore@DESKTOP-36JK8EO:~/data$ cat rfile.txt
asaishishidh
kishore@DESKTOP-36JK8EO:~/data$ ls
demo.txt  new_hello.txt  rfile.txt
kishore@DESKTOP-36JK8EO:~/data$ echo "Kishorelytics"
Kishorelytics
kishore@DESKTOP-36JK8EO:~/data$ echo "Kishore Founder and CEO of Kishorelytics" >> rfile.txt
kishore@DESKTOP-36JK8EO:~/data$ s
s: command not found
kishore@DESKTOP-36JK8EO:~/data$ ls
demo.txt  new_hello.txt  rfile.txt
kishore@DESKTOP-36JK8EO:~/data$ cat rfile.txt
asaishishidh
Kishore Founder and CEO of Kishorelytics

kishore@DESKTOP-36JK8EO:~/data$ history >> history.txt
kishore@DESKTOP-36JK8EO:~/data$ ls
demo.txt  history.txt  new_hello.txt  rfile.txt
kishore@DESKTOP-36JK8EO:~/data$ cat history.txt
    1  pwd
    2  0868
    3  exit
    4  pwd
    5  uname -a
    6  whoami
    7  clear
    8  history
    9  clear
   10  mkdir data
   11  cd data
   12  cd data/
   13  exit
   14  clear
   15  mkdir data
   16  cd data
   17  vi hello.txt
   18  ls
   19  pwd
   20  vi hello.txt
   21  sudo apt-get install vim
   22  cd
   23  clear
   24  vi hello.txt
   25  vi hello1.txt
   26  vls
   27  ls
   28  cd data/
   29  ls
   30  vi Hitest.py
   31  ls
   32  nano test.txt
   33  ls
   34  vi hello.txt
   35  vi hello.txt
   36  touch foo.txt
   37  ls
   38  rm foo.txt
   39  ls *.txt
   40  rm *.txt
   41  ls
   42  rm *
   43  ls
   44  vi hello.txt
   45  cat hello.txt
   46  clear
   47  ls
   48  cat hello.txt new_hello.txt
   49  cp hello.txt new_hello.txt
   50  ls
   51  cat new_hello.txt
   52  mv hello.txt demo.txt
   53  ls
   54  cat demo.txt >> rfile.txt
   55  ls
   56  cat rfile.txt
   57  ls
   58  echo "Kishorelytics"
   59  echo "Kishore Founder and CEO of Kishorelytics" >> rfile.txt
   60  s
   61  ls
   62  cat rfile.txt
   63  history >> history.txt

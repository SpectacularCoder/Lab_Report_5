# -cse-15l-lab-report-week9
## Lab Report 5
### Researching Commands For Find
### Command 1: 
**find ./directory -empty** this command searches a directory and finds all the empty files in the directory or sub-directories

**Example 1:**

**Command Line Argument:**
This command seraches in the root directory docsearch-main/ for any empty files 
```
#code block
$ find ./docsearch-main/ -empty
```

**Output:**
The files inside this directory that are empty is returned
```
#code block
./docsearch-main/lib/docsearch/.git/objects/info
./docsearch-main/lib/docsearch/.git/refs/tags
./docsearch-main/lib/docsearch/berliztChar.txt
./docsearch-main/lib/docsearch/Kauffman_sizes.txt
```
**Example 2:**
**Command Line Argument:**
This command searches for empty files in the subdirectory lib/
```
#code block
$ find ./lib/ -empty
```
**Output:**
The specific files are returned, however this time it dies not include docsearch-main. Instead, it starts off the output with ./lib this time\
```
#code block
./lib/docsearch/.git/objects/info
./lib/docsearch/.git/refs/tags
./lib/docsearch/berliztChar.txt
./lib/docsearch/Kauffman_sizes.txt
```

***Source***: **[geekforgeeks grep command in Unix/Linux](https://www.geeksforgeeks.org/find-command-in-linux-with-examples/)**

### Command 2: 
**find -size +(insert data size)M or find -size(insert data size)M** this command searches a directory and finds files larger than the specified sizes or at specific size

**Example 1:**

**Command Line Argument:**
This command searches the directory for any files larger than 2M or 2 megabytes. MB is denoted in M. The plus sign is necessary for the find command to recgonize it needs to find files larger than M.
```
#code block
$find -size +2M
```
**Output:**
The specific files with greater than 2 megabytes are returned
```
#code block
./docsearch-main/lib/docsearch/.git/
objects/pack/pack-fb18ac1d05cceddf8f26d30962d4e4068d27ae87.pack
```
**Example 2:**
**Command Line Argument:**
This command, searches for a file at 1 MB. Instead of finding one bigger, this command finds files exactly as specified.
```
#code block
$find -size 1M
```
**Output:**
The specific files are returned, the command does not utilize a + sign to denote it want files greater than 1MB.
```
#code block
./docsearch-main/DocSearchServer.java
./docsearch-main/lib/docsearch/.find-results.txt.swp
./docsearch-main/lib/docsearch/.git/COMMIT_EDITMSG
./docsearch-main/lib/docsearch/.git/config
./docsearch-main/lib/docsearch/.git/description
./docsearch-main/lib/docsearch/.git/FETCH_HEAD
./docsearch-main/lib/docsearch/.git/HEAD
./docsearch-main/lib/docsearch/.git/hooks/applypatch-msg.sample
...
```

***Source***: **[Geekflare's 40 Examples of Using Find Command](https://geekflare.com/linux-find-commands/)**

### Command 3: 
**$ find . -mtime -(days) -type f** this command searches for files that has been modified within a certain time period

**Example 1:**

**Command Line Argument:**
This command seraches in the root directory docsearch-main/ for files that have been modified in the last 30 days
```
#code block
$ find . -mtime -30 -type f
```

**Output:**
The files inside this directory that are modified within the last 30 days are returned
```
#code block
...
```
**Example 2:**
**Command Line Argument:**
This command searches for directories modified in the last 30 days
```
#code block
$ find . -mtime -30 -type d
```
**Output:**
The specific files are returned, however this time it is searching for directories only. This is done by changing type f to type d.
```
#code block
./docsearch-main
./docsearch-main/lib
./docsearch-main/lib/docsearch
./docsearch-main/lib/docsearch/.git
./docsearch-main/lib/docsearch/.git/hooks
./docsearch-main/lib/docsearch/.git/info
./docsearch-main/lib/docsearch/.git/logs
./docsearch-main/lib/docsearch/.git/logs/refs
./docsearch-main/lib/docsearch/.git/logs/refs/heads
./docsearch-main/lib/docsearch/.git/logs/refs/remotes
./docsearch-main/lib/docsearch/.git/logs/refs/remotes/origin
./docsearch-main/lib/docsearch/.git/objects
./docsearch-main/lib/docsearch/.git/objects/0b
./docsearch-main/lib/docsearch/.git/objects/2d
./docsearch-main/lib/docsearch/.git/objects/33
./docsearch-main/lib/docsearch/.git/objects/3a
./docsearch-main/lib/docsearch/.git/objects/3b
./docsearch-main/lib/docsearch/.git/objects/44
./docsearch-main/lib/docsearch/.git/objects/58
./docsearch-main/lib/docsearch/.git/objects/59
./docsearch-main/lib/docsearch/.git/objects/93
./docsearch-main/lib/docsearch/.git/objects/a3
./docsearch-main/lib/docsearch/.git/objects/ce
./docsearch-main/lib/docsearch/.git/objects/e6
./docsearch-main/lib/docsearch/.git/objects/eb
./docsearch-main/lib/docsearch/.git/objects/info
./docsearch-main/lib/docsearch/.git/objects/pack
./docsearch-main/lib/docsearch/.git/refs
./docsearch-main/lib/docsearch/.git/refs/heads
./docsearch-main/lib/docsearch/.git/refs/remotes
./docsearch-main/lib/docsearch/.git/refs/remotes/origin
./docsearch-main/lib/docsearch/.git/refs/tags
./docsearch-main/lib/docsearch/lib
./docsearch-main/lib/docsearch/written_2
./docsearch-main/lib/docsearch/written_2/non-fiction
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Abernathy
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Berk
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Castro
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Fletcher
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Kauffman
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Rybczynski
./docsearch-main/lib/docsearch/written_2/travel_guides
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz2
./docsearch-main/written_2
./docsearch-main/written_2/non-fiction
./docsearch-main/written_2/non-fiction/OUP
./docsearch-main/written_2/non-fiction/OUP/Abernathy
./docsearch-main/written_2/non-fiction/OUP/Berk
./docsearch-main/written_2/non-fiction/OUP/Castro
./docsearch-main/written_2/non-fiction/OUP/Fletcher
./docsearch-main/written_2/non-fiction/OUP/Kauffman
./docsearch-main/written_2/non-fiction/OUP/Rybczynski
./docsearch-main/written_2/travel_guides
./docsearch-main/written_2/travel_guides/berlitz1
./docsearch-main/written_2/travel_guides/berlitz2

```
***Source***: **[Geekflare's 40 Examples of Using Find Command](https://geekflare.com/linux-find-commands/)**

### Command 4: 
**$ find . -amin -(time in minutes) -type f** this command searches for files accessed within a certain minute
**Example 1:**

**Command Line Argument:**
This command seraches in the root directory docsearch-main/ for any files accessed within the last 10 minutes
```
#code block
$find . -amin -10 -type f
```

**Output:**
The files that haven been accessed within the last 10 minutes are returned
```
#code block
./docsearch-main/DocSearchServer.java
./docsearch-main/lib/docsearch/.find-results.txt.swp
./docsearch-main/lib/docsearch/.git/COMMIT_EDITMSG
./docsearch-main/lib/docsearch/.git/config
./docsearch-main/lib/docsearch/.git/description
./docsearch-main/lib/docsearch/.git/FETCH_HEAD
./docsearch-main/lib/docsearch/.git/HEAD
./docsearch-main/lib/docsearch/.git/hooks/applypatch-msg.sample
./docsearch-main/lib/docsearch/.git/hooks/commit-msg.sample
./docsearch-main/lib/docsearch/.git/hooks/fsmonitor-watchman.sample
./docsearch-main/lib/docsearch/.git/hooks/post-update.sample
./docsearch-main/lib/docsearch/.git/hooks/pre-applypatch.sample
./docsearch-main/lib/docsearch/.git/hooks/pre-commit.sample
./docsearch-main/lib/docsearch/.git/hooks/pre-merge-commit.sample
./docsearch-main/lib/docsearch/.git/hooks/pre-push.sample
./docsearch-main/lib/docsearch/.git/hooks/pre-rebase.sample
./docsearch-main/lib/docsearch/.git/hooks/pre-receive.sample
./docsearch-main/lib/docsearch/.git/hooks/prepare-commit-msg.sample
./docsearch-main/lib/docsearch/.git/hooks/push-to-checkout.sample
./docsearch-main/lib/docsearch/.git/hooks/update.sample
./docsearch-main/lib/docsearch/.git/index
./docsearch-main/lib/docsearch/.git/info/exclude
./docsearch-main/lib/docsearch/.git/logs/HEAD
./docsearch-main/lib/docsearch/.git/logs/refs/heads/main
./docsearch-main/lib/docsearch/.git/logs/refs/remotes/origin/HEAD
./docsearch-main/lib/docsearch/.git/logs/refs/remotes/origin/main
./docsearch-main/lib/docsearch/.git/objects/0b/8f1bc15f56fc83553abc1d2aa59e2a4cd6fa3b
./docsearch-main/lib/docsearch/.git/objects/2d/3b4b7b0a113b19192479070973f363f1d277a6
./docsearch-main/lib/docsearch/.git/objects/33/f9a22dce0c919dc3d8706f9b7aaec8a4f49eb0
./docsearch-main/lib/docsearch/.git/objects/3a/5d0aeb70683e8225a8b7889cd8f2f54dae2d91
./docsearch-main/lib/docsearch/.git/objects/3b/fdf6b7b568510518ea0d183e00df5a39c3f3b6
./docsearch-main/lib/docsearch/.git/objects/44/8e963f1eaf050990e4f95983a5811c1c150904
./docsearch-main/lib/docsearch/.git/objects/58/1bb12c80735b5cbbe40c50224e2e2315468fee
./docsearch-main/lib/docsearch/.git/objects/59/eeeb1a2d2ca1ced105f4c2f1ebec0fe16a848a
./docsearch-main/lib/docsearch/.git/objects/93/826328488435853c63b941fa754f38ccd2e975
./docsearch-main/lib/docsearch/.git/objects/a3/8caf95c016a79925a605d1144f6acbed433169
./docsearch-main/lib/docsearch/.git/objects/ce/16bf3879069cd4772cd2d0984c1e87e6979b51
./docsearch-main/lib/docsearch/.git/objects/e6/9de29bb2d1d6434b8b29ae775ad8c2e48c5391
./docsearch-main/lib/docsearch/.git/objects/eb/0c114766f7e212ff7aade80f4714ccaaf18d56
./docsearch-main/lib/docsearch/.git/objects/pack/pack-fb18ac1d05cceddf8f26d30962d4e4068d27ae87.idx
./docsearch-main/lib/docsearch/.git/objects/pack/pack-fb18ac1d05cceddf8f26d30962d4e4068d27ae87.pack
./docsearch-main/lib/docsearch/.git/packed-refs
./docsearch-main/lib/docsearch/.git/refs/heads/main
./docsearch-main/lib/docsearch/.git/refs/remotes/origin/HEAD
./docsearch-main/lib/docsearch/.git/refs/remotes/origin/main
./docsearch-main/lib/docsearch/berlitz1Char.txt
./docsearch-main/lib/docsearch/berlitz2Char.txt
./docsearch-main/lib/docsearch/count-txts.sh
./docsearch-main/lib/docsearch/DocSearchServer.java
./docsearch-main/lib/docsearch/find-results.txt
./docsearch-main/lib/docsearch/grep-results.txt
./docsearch-main/lib/docsearch/lib/hamcrest-core-1.3.jar
./docsearch-main/lib/docsearch/lib/junit-4.13.2.jar
./docsearch-main/lib/docsearch/README.md
./docsearch-main/lib/docsearch/Server.java
./docsearch-main/lib/docsearch/TestDocSearch.java
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Abernathy/ch1.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Abernathy/ch14.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Abernathy/ch15.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Abernathy/ch2.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Abernathy/ch3.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Abernathy/ch6.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Abernathy/ch7.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Abernathy/ch8.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Abernathy/ch9.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Berk/ch1.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Berk/ch2.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Berk/CH4.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Berk/ch7.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Castro/chA.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Castro/chB.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Castro/chC.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Castro/chL.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Castro/chM.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Castro/chN.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Castro/chO.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Castro/chP.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Castro/chQ.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Castro/chR.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Castro/chV.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Castro/chW.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Castro/chY.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Castro/chZ.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Fletcher/ch1.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Fletcher/ch10.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Fletcher/ch2.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Fletcher/ch5.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Fletcher/ch6.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Fletcher/ch9.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Kauffman/ch1.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Kauffman/ch10.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Kauffman/ch3.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Kauffman/ch4.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Kauffman/ch5.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Kauffman/ch6.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Kauffman/ch7.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Kauffman/ch8.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Kauffman/ch9.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Rybczynski/ch1.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Rybczynski/ch2.txt
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Rybczynski/ch3.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HandRHawaii.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HandRHongKong.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HandRIbiza.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HandRIsrael.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HandRIstanbul.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HandRJamaica.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HandRJerusalem.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HandRLakeDistrict.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HandRLasVegas.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HandRLisbon.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HandRLosAngeles.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HandRMadeira.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HandRMadrid.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HandRMallorca.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HistoryDublin.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HistoryEdinburgh.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HistoryEgypt.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HistoryFrance.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HistoryFWI.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HistoryGreek.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HistoryHawaii.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HistoryHongKong.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HistoryIbiza.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HistoryIndia.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HistoryIsrael.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HistoryIstanbul.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HistoryItaly.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HistoryJamaica.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HistoryJapan.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HistoryJerusalem.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HistoryLakeDistrict.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HistoryLasVegas.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HistoryMadeira.txt
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1/HistoryMadrid.txt
...
```
**Example 2:**
**Command Line Argument:**
This command searches directories that have been accessed within the last 10 minutes
```
#code block
$ find . -amin -10 -type d
```
**Output:**
The specific files are returned, however this it is looking for directories and not files
```
#code block
.
./docsearch-main
./docsearch-main/lib
./docsearch-main/lib/docsearch
./docsearch-main/lib/docsearch/.git
./docsearch-main/lib/docsearch/.git/hooks
./docsearch-main/lib/docsearch/.git/info
./docsearch-main/lib/docsearch/.git/logs
./docsearch-main/lib/docsearch/.git/logs/refs
./docsearch-main/lib/docsearch/.git/logs/refs/heads
./docsearch-main/lib/docsearch/.git/logs/refs/remotes
./docsearch-main/lib/docsearch/.git/logs/refs/remotes/origin
./docsearch-main/lib/docsearch/.git/objects
./docsearch-main/lib/docsearch/.git/objects/0b
./docsearch-main/lib/docsearch/.git/objects/2d
./docsearch-main/lib/docsearch/.git/objects/33
./docsearch-main/lib/docsearch/.git/objects/3a
./docsearch-main/lib/docsearch/.git/objects/3b
./docsearch-main/lib/docsearch/.git/objects/44
./docsearch-main/lib/docsearch/.git/objects/58
./docsearch-main/lib/docsearch/.git/objects/59
./docsearch-main/lib/docsearch/.git/objects/93
./docsearch-main/lib/docsearch/.git/objects/a3
./docsearch-main/lib/docsearch/.git/objects/ce
./docsearch-main/lib/docsearch/.git/objects/e6
./docsearch-main/lib/docsearch/.git/objects/eb
./docsearch-main/lib/docsearch/.git/objects/info
./docsearch-main/lib/docsearch/.git/objects/pack
./docsearch-main/lib/docsearch/.git/refs
./docsearch-main/lib/docsearch/.git/refs/heads
./docsearch-main/lib/docsearch/.git/refs/remotes
./docsearch-main/lib/docsearch/.git/refs/remotes/origin
./docsearch-main/lib/docsearch/.git/refs/tags
./docsearch-main/lib/docsearch/lib
./docsearch-main/lib/docsearch/written_2
./docsearch-main/lib/docsearch/written_2/non-fiction
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Abernathy
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Berk
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Castro
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Fletcher
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Kauffman
./docsearch-main/lib/docsearch/written_2/non-fiction/OUP/Rybczynski
./docsearch-main/lib/docsearch/written_2/travel_guides
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz1
./docsearch-main/lib/docsearch/written_2/travel_guides/berlitz2
./docsearch-main/written_2
./docsearch-main/written_2/non-fiction
./docsearch-main/written_2/non-fiction/OUP
./docsearch-main/written_2/non-fiction/OUP/Abernathy
./docsearch-main/written_2/non-fiction/OUP/Berk
./docsearch-main/written_2/non-fiction/OUP/Castro
./docsearch-main/written_2/non-fiction/OUP/Fletcher
./docsearch-main/written_2/non-fiction/OUP/Kauffman
./docsearch-main/written_2/non-fiction/OUP/Rybczynski
./docsearch-main/written_2/travel_guides
./docsearch-main/written_2/travel_guides/berlitz1
./docsearch-main/written_2/travel_guides/berlitz2
```
***Source***: **[Geekflare's 40 Examples of Using Find Command](https://geekflare.com/linux-find-commands/)**

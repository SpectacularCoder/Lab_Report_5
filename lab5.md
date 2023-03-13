# -cse-15l-lab-report-week9
## Lab Report 5
### Researching Commands For Less
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

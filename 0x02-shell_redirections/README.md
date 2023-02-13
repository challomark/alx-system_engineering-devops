echo "Hello World" prints “Hello, World”, followed by a new line to the standard output.
echo "\"(Ôo)'" displays a confused smiley.
cat /etc/passwd displays the content of the /etc/passwd file.
cat /etc/{passwd,hosts} displays content of /etc/passwd and /etc/hosts.
tail -n 10 /etc/passwd displays the last 10 lines of /etc/passwd.
head -n 10 /etc/passwd displays the first 10 lines of etc/passwd.
cat iacta | head -n 3 | tail -n 1 displays the third line of the file iacta. The file iacta will be in the working directory and you are not allowed to use sed.
echo "Best School" > "\*\\\'\"Best School\"\'\\\*$\?\*\*\*\*\*:)"
ls -la > ls_cwd_content writes into the file ls_cwd_content the result of the command ls -la. If the file ls_cwd_content already exists, it should be overwritten. If the file ls_cwd_content does not exist, create it.
tail -n 1 iacta >> iacta duplicates the last line of the file iacta.
find . -name '*.js' -type f -delete deletes all the regular files (not the directories) with a .js extension that are present in the current directory and all its subfolders.
find . -mindepth 1 -type d | wc -l counts the number of directories and sub-directories in the current directory. The current and present directories should not be taken into account. Hidden directories should be counted. 
ls -t | head -n 10 prints the 10 newest files in the current directory. The output should be; one file per line and sorted from the newest to the oldest.
sort | uniq -u takes a list of words as input and prints only words that appear exactly once.
grep root /etc/passwd prints lines containing the pattern "root" from the file /etc/passwd.
grep bin /etc/passwd | wc -l displays the number of lines that contain the pattern "bin" in the file /etc/passwd.
grep -A 3 'root' /etc/passwd displays lines containing the pattern “root” and 3 lines after them in the file /etc/passwd.
grep -v bin /etc/passwd displays all the lines in the file /etc/passwd that do not contain the pattern “bin”.
grep '^[[:upper:]]\|^[[:lower:]]' /etc/ssh/sshd_config displays all lines of the file /ect/ssh/sshd_config starting with a letter, including capital letters as well.
tr Ac Ze replaces all characters A and C from input to Z and E respectively.
tr -d cC removes all letters c and C from input.
rev reverse its input.
cut -d':' -f1,6  /etc/passwd | sort displays all users and their home directories, sorted by users.
find . -empty -printf '%f\n' finds all empty files and directories in the current directory and all sub-directories. Only the names of the files and directories should be displayed (not the entire path), Hidden files should be listed, One file name per line, The listing should end with a new line, You are not allowed to use basename, grep, egrep, fgrep or rgrep.
find -type f -name "*.gif" | rev | cut -d "/" -f 1 | cut -d '.' -f 2- | rev | LC_ALL=C sort -f lists all the files with a .gif extension in the current directory and all its sub-directories, Hidden files should be listed, Only regular files (not directories) should be listed, The names of the files should be displayed without their extensions, The files should be sorted by byte values, but case-insensitive (file aaa should be listed before file bbb, file .b should be listed before file a, and file Rona should be listed after file jay), One file name per line, The listing should end with a new line, You are not allowed to use basename, grep, egrep, fgrep or rgrep.
cut -c 1 | paste -s -d '' decodes acrostics that use the first letter of each line, The ‘decoded’ message has to end with a new line, You are not allowed to use grep, egrep, fgrep or rgrep.
tail -n +2 | cut -f -1 | sort -k 1 | uniq -c | sort -rnk 1 | head -n 11 | rev | cut -d ' ' -f -1 | rev parses web servers logs in TSV format as input and displays the 11 hosts or IP addresses which did the most requests. Order by number of requests, most active host or IP at the top, You are not allowed to use grep, egrep, fgrep or rgrep.

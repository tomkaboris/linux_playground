1. CAT(concatenate) command is very frequently used in Linux. It reads data from the file and gives its content as output.

    [example]

| To view a single file |
| -------------- |
```bash
cat file.txt
```
| To view multiple files |
| -------------- |
```bash
cat file1.txt file2.txt
```
| To view contents of file preceding with line numbers |
| -------------- |
```bash
cat -n file.txt
```
| Create file and add content |
| -------------- |
```bash
cat > new_file.txt
```
| Copy the content of one file to another |
| -------------- |
```bash
cat file_one.txt > file_two.txt
```
| Append content of one file to another |
| -------------- |
```bash
cat file_one.txt >> file_two.txt
```
| Display content in reverse order |
| -------------- |
```bash
tac file.txt
```
| Cat command to open dash files |
| -------------- |
```bash
cat -- '-dashfile'
```
| Cat command to merge multiple files |
| -------------- |
```bash
cat file1.txt file2.txt file3.txt > merged_filename
```
| Cat command to write on already existing file | 
| -------------- |
```bash
cat >> file.txt
```

    | Example        | Description    |
    | -------------- | -------------- |
    | `cat file.txt` | To view a single file |
    | `cat file1.txt file2.txt` | To view multiple files |
    | `cat -n file.txt` | To view contents of file preceding with line numbers | 
    | `cat > new_file.txt` | Create file and add content |
    | `cat file_one.txt > file_two.txt` | Copy the content of one file to another |
    | `cat file_one.txt >> file_two.txt` | Append content of one file to another |
    | `tac file.txt` | Display content in reverse order |
    | `cat -- "-dashfile"` | Cat command to open dash files |
    | `cat "file1.txt" "file2.txt" "file3.txt" > "merged_filename"` | Cat command to merge multiple files |
    | `cat >> file.txt` | Cat command to write on already existing file |


2. GREP filter searches a file for a particular pattern of characters, and displays all lines that contain that pattern. 

    | Example        | Description    |
    | -------------- | -------------- |
    | `grep -i "Linux" file.txt` | Case insensitive search |
    | `grep -c "Linux" file.txt` | Displaying the count of number of matches |
    | `grep -l "Linux" *` | Display the file names that matches the pattern |
    | `grep -w "Linux" file.txt` | Checking for the whole words in a file |
    | `grep -o "Linux" file.txt` | Displaying only the matched pattern |
    | `grep -n "Linux" file.txt` | Show line number while displaying the output |
    | `grep -v "Linux" file.txt` | Display the lines that are not matched with the specified search string pattern |
    | `grep "^Linux" file.txt` | Matching the lines that start with a string |
    | `grep "Linux$" geekfile.txt` | Matching the lines that end with a string |
    | `grep –e "Linux" -e "Unix" -e "Command" file.txt` | Specifies expression with -e option, canan use multiple times |
    | `$grep -A[NumberOfLines(n)] Linux file.txt` | Print number of specific lines from a file [n lines after result] |
    | `$grep -B[NumberOfLines(n)] Linux file.txt` | Print number of specific lines from a file [n lines before result] |
    | `$grep -C[NumberOfLines(n)] Linux file.txt` | Print number of specific lines from a file [n lines after and before result] |
    | `grep -R "Linux" file.txt` | Search recursively for a pattern in the directory |


3. SED command in UNIX stands for stream editor and it can perform lots of functions on file like searching, find and replace, insertion or deletion.

    | Example        | Description    |
    | -------------- | -------------- |
    | `sed 's/unix/linux/' file.txt` | Replacing or substituting string |
    | `sed 's/unix/linux/2' file.txt` | Replacing the n occurrence of a pattern in a line. The below command replaces the second occurrence of the word “unix” with “linux” in a line.  |
    | `sed 's/unix/linux/g' file.txt` | Replacing all the occurrence of the pattern in a line |
    | `sed '3 s/unix/linux/' file.txt` | Replacing string on a specific line number |
    | `sed '1,3 s/unix/linux/' file.txt` | Replacing string on a range of lines |
    | `sed '5d' file.txt` | Deleting particular line lines from a particular file |
    | `sed '$d' file.txt` | Delete a last line |
    | `sed '3,6d' file.txt` | To Delete line from range x to y |
    | `sed '12,$d' file.txt` | To Delete from n line to last line |
    | `sed '/command/d' file.txt` | To Delete pattern matching line |
    

4. AWK is a scripting language used for manipulating data and generating reports.

    | Example        | Description    |
    | -------------- | -------------- |
    | `awk '/Linux/ {print}' file.txt` | Print the lines which match the given pattern. |
    | `awk '{print $1,$4}' file.txt` | Splitting a Line Into Fields, delimited by whitespace character by default. |
    | `awk '{print NR "- " $1 }' file.txt` | To print the first item along with the row number(NR) separated with ” – “ from each line in file.txt |
    | `awk 'NF < 0' file.txt` | To print any non empty line if present |
    | `awk '{ if (length($0) > max) max = length($0) } END { print max }' file.txt` | To find the length of the longest line present in the file |
    | `awk 'END { print NR }' file.txt` | To count the lines in a file |
    | `awk 'length($0) > 10' file.txt` | Printing lines with more than 10 characters |


5. TOP command is used to show the Linux processes. It provides a dynamic real-time view of the running system.

    | Example        | Description    |
    | -------------- | -------------- |
    | `top -n 10` | With below command top command will automatically exit after 10 number of repetition |
    | `top -u root` | Display specific user process |
    | `top -b` | Send output from top to file or any other programs. |
    | `top -s` | Use top in Secure mode. |
    

    | Example While TOP is running | Description    |
    | ---------------------------- | -------------- |
    | z | Press 'z' option in running top command will display running process in color which may help you to identified running process easily. |
    | c | Press 'c' option in running top command, it will display absolute path of running process. |
    | k | You can kill a process after finding PID of process by pressing 'k' option in running top command without exiting from top window as shown below. |
    | Shift+P | Press (Shift+P) to sort processes as per CPU utilization. |
    | o | Press 'o' and search proces by any parametar that is given in top command. |


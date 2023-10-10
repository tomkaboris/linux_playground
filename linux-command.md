1. Cat(concatenate) command is very frequently used in Linux. It reads data from the file and gives its content as output.

    [options]
    - -A, --show-all           equivalent to -vET
    - -b, --number-nonblank    number nonempty output lines, overrides -n
    - -e                       equivalent to -vE
    - -E, --show-ends          display $ at end of each line
    - -n, --number             number all output lines
    - -s, --squeeze-blank      suppress repeated empty output lines
    - -t                       equivalent to -vT
    - -T, --show-tabs          display TAB characters as ^I
    - -u                       (ignored)
    - -v, --show-nonprinting   use ^ and M- notation, except for LFD and TAB

    [examples]
    - To view a single file
    `cat file.txt`
    - To view multiple files
    `cat file1.txt file2.txt`
    - To view contents of file preceding with line numbers
    `cat -n file.txt`
    - Create file and add content
    `cat > new_file.txt`
    - Copy the content of one file to another
    `cat file_one.txt > file_two.txt`
    - Append content of one file to another
    `cat file_one.txt >> file_two.txt`
    - Display content in teverse order
    `tac file.txt`
    - Highlight the end of line
    `cat -E file.txt`
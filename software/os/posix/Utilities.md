

[wikipedia: List of posix commands](https://en.wikipedia.org/wiki/List_of_POSIX_commands)

# rm
released in Unix V1

## usage
- To remove all the contents of the folder but not the folder itself:
  ```
  rm -rf /path/to/directory/*
  ```
# pwd
- [Basically, `$pwd` is just where the shell thinks you are, not necessarily where you really are](https://unix.stackexchange.com/questions/295495/ls-pwd-and-ls-get-different-files-strange-caching-perhaps/295497#295497)
  - This can happen if the current directory is renamed or moved while you're in it.

# tr

## usage
- 从大写转化到小写`ORG=echo ${ORG} | tr '[:upper:]' '[:lower:]'`

# cat
`cat` for (concatenate)
- 用于连接文件并输出内容

# vi
- available when system has POSIX2_CHAR_TERM signal definition
https://github.com/davidkhala/linux-utils/wiki

# tail
- follow and attach to current terminal: `tail -f`
- get last line: `tail -1`

# [cut](https://man7.org/linux/man-pages/man1/cut.1.html)
Print selected parts of bytes/chars/lines from each FILE(or standard input) to standard output.
- Similar to `awk` in some use cases.
- Required: Use one, and only one of `-b`, `-c` or `-f`
- `-d`: --delimiter. Use specified delimiter instead of TAB for field delimiter
- `-b`: --bytes. Select only these bytes
- `-f`: --fields. Select only these fields
  - Also print any line that contains no delimiter character, unless the `-s` option is specified
  - Example: `echo a-b-c | cut -d"-" -f1,3` will stdout `a-c`
# date
[blog:How To Format Date For Display](https://www.cyberciti.biz/faq/linux-unix-formatting-dates-for-display/)
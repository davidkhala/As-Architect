# POSIX shell

[The Open Group: Shell Command Language](https://pubs.opengroup.org/onlinepubs/9799919799/)

# syntax

- `$@` is all of the parameters passed to the script.
  - For instance, if you call `./someScript.sh foo bar` then `$@` will be equal to `foo bar`.

## I/O operators
- `<`
  - > redirecting input to a source other than the keyboard
  - 将一个文件的内容作为命令的标准输入 (替换式)
- `>`
  - > redirecting output to destination other than the screen
- `>>`
  - > redirecting output to destination other than the screen, but by appending rather than overwriting
- `<<<`: 字符串作为命令的标准输入
- `<<`: EOF标记关键字
- `|`
  - > piping output from one command to the input of another


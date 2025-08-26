# POSIX shell

[The Open Group: Shell Command Language](https://pubs.opengroup.org/onlinepubs/9799919799/)


# syntax

- `$@` is all of the parameters passed to the script.
  - For instance, if you call `./someScript.sh foo bar` then `$@` will be equal to `foo bar`.
- 箭头符号 `>` 与 `<` （Ref: <https://blog.csdn.net/dapeng1994/article/details/84311357）>
  - <<<: 字符串作为命令的标准输入
  - <<: EOF标记关键字
  - < : 将一个文件的内容作为命令的标准输入 (替换式)

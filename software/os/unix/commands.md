list of common but non-POSIX commands

# ping
1983, Michael John Muuss, Ballistic Research Laboratory(美国陆军弹道实验室)

## usage
`ping -c <count of try times> <ip>`

# curl
1997, Daniel Stenberg, Sweden
- Daniel 当时参与一个 IRC 聊天机器人项目，需要从网页上抓取汇率数据
- 最初项目名叫 httpget，只支持 HTTP 协议，用于从网页下载数据。
- renamed as curl in 1998 with FTP and Gopher support added

# usage
- `curl <url> | bash -s <function>`
  - Your target function cannot inherit STDIN of the caller context.
  - Thus if your function include interactive command like `expect`, `passwd`, then can only be executed in local.
  - about `bash -s`, please go to [bash usage](./GNU/bash.md#usage) 

# less

Compared to [`more`](#more)
- 支持正则搜索
  - 使用 `/pattern` 向下查找
  - `?pattern` 向上查找。
- 直接查看压缩文件
- 按需加载，适合查看大文件
- 退出后不会在终端留下文件内容

# [more](https://man7.org/linux/man-pages/man1/more.1.html)
- exit: `q`
- page down: `<SPACE>`
- one line down: `<ENTER>`
- page up: `b`
- no way to one line up


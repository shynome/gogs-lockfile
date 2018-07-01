
# install

- 下载 `lock` 文件
- 添加可执行权限 `chmod +x lock`
- 把 `lock` 文件移动到 `/usr/bin` 之类的环境变量目录下, 保证能够全局调用

命令行安装
```sh
f=/usr/bin/lock && \
wget -O $f https://raw.githubusercontent.com/shynome/gogs-lockfile/master/lock && \
chmod +x $f
```

# Usage

编辑 `pre-commit` 文件:
```sh 
#!/bin/sh
# set -e 出现错误立即退出
set -e
# 读取 prev_commit_sha 和 next_commit_sha
read input
# lock 文件,文件,1文件 提交者,提交者
echo $input | lock .drone.yml,aa,cc shynome,nuome
echo $input | lock .drone.yml,aa,cc shynome,nuome
```


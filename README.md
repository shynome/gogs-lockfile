
# install

- 下载 `lock` 文件
- 添加可执行权限 `chmod +x lock`
- 把 `lock` 文件移动到 `/usr/bin` 之类的环境变量目录下, 保证能够全局调用

命令行安装
```sh
f=/usr/bin/lock && \
wget -o $f https://gist.github.com/shynome/7717d226ec50a123f02481bdcb7fe76b/raw/dc93484c181c6480eebf5b8894357900e66d9063/lock && \
chmod +x $f
```

# Usage

编辑 `pre-commit` 文件:
```sh
lock .drone.yml,aa,cc shynome,nuome
```


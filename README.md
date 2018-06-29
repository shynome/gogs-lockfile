# Usage

首先把 `lock` 加入到 `/usr/bin` 之类的环境变量目录下, 保证能够全局调用

编辑 `pre-commit` 文件:
```sh
lock .drone.yml,aa,cc shynome,nuome
```
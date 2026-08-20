# uv 管理 Python 项目

使用 uv 可以方便的管理 Python 项目及其依赖

# 初始化项目

在项目目录中初始化一个 uv 管理的 Python 项目：

```shell
uv init . --bare --python 3.10
```

参数说明：

- `--bare`：创建基本的项目结构
- `--python 3.10`：指定项目使用的 Python 版本

# 锁定 Python 版本

修改 `pyproject.toml` 文件中的 `requires-python`，锁定 Python 大版本：

```toml
requires-python = "==3.10.*"
```

# 同步项目

根据 `pyproject.toml` 文件和 `uv.lock` 文件安装项目依赖，并创建或更新虚拟环境：

```shell
uv sync
```

> 如果项目中不存在 `uv.lock`，`uv sync` 会自动创建

# 管理依赖

添加依赖：

```shell
uv add <pkg-name>
```

删除依赖：

```shell
uv remove <pkg-name>
```

# 运行项目

使用 uv 运行 Python 项目：

```shell
uv run main.py
```

> 会自动使用当前项目的虚拟环境运行



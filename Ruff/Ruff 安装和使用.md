# Ruff 安装和使用

使用 Ruff 是为了规范 Python 项目的代码质量和代码风格

# 安装和查看 Ruff

使用 `uv` 将 Ruff 添加为项目的开发依赖：

```shell
uv add --dev ruff
```

查看 Ruff 版本：

```shell
uv run ruff --version
```

# 代码检查

使用 `ruff check` 检查代码，可以指定文件、目录或整个项目

检查整个项目代码：

```shell
uv run ruff check .
```

检查整个项目代码，并自动修复可修复的问题：

```shell
uv run ruff check . --fix
```

# 代码格式化

使用 `ruff format` 格式化代码，可以指定文件、目录或整个项目

格式化整个项目代码：

```shell
uv run ruff format .
```

检查整个项目代码格式，但不修改文件：

```shell
uv run ruff format . --check
```



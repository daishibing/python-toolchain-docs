# ty 安装和使用

使用 ty 是为了检查 Python 项目的类型问题，提高代码可靠性

# 安装和查看 ty

使用 `uv` 将 ty 添加为项目的开发依赖：

```shell
uv add --dev ty
```

查看 ty 版本：

```shell
uv run ty --version
```

# 类型检查

使用 `ty check` 检查代码，可以指定文件、目录或整个项目

ty 只负责检查类型问题，不会自动修改代码

检查整个项目代码：

```shell
uv run ty check .
```



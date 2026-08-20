# uv 安装和管理

安装和管理 uv 是为了给 Python 项目提供工程化支持

# 安装 uv

macOS 和 Linux：

```shell
curl -LsSf https://astral.sh/uv/install.sh | sh
```

Windows：

```shell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

# 管理 uv

查看 uv 版本：

```shell
uv --version
```

更新 uv 版本：

```shell
uv self update
```

卸载 uv：

```shell
uv self uninstall
```

> 卸载 uv 不代表使用 uv 安装的 Python 也卸载



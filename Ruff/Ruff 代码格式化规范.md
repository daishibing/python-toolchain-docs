# Ruff 代码格式化规范

Ruff 提供了 Python 代码格式化功能，可以统一代码的缩进、引号、换行等格式，配合 `ruff format` 命令使用

# 常用配置

| 配置项                   | 推荐值    | 作用                 | 使用原因                        |
|-----------------------|--------|--------------------|-----------------------------|
| quote-style           | double | 设置字符串引号            | 统一使用双引号                     |
| indent-style          | space  | 设置缩进方式             | 使用空格缩进，符合 Python 社区规范       |
| line-ending           | lf     | 设置换行符              | 统一使用 LF，避免不同操作系统产生换行符差异     |
| docstring-code-format | true   | 格式化 docstring 中的代码 | 统一 docstring 中 Python 代码的格式 |

# 格式化配置

将常用配置添加到 uv 管理的 `pyproject.toml` 文件中：

```toml
[tool.ruff.format]
quote-style = "double"
indent-style = "space"
line-ending = "lf"
docstring-code-format = true
```



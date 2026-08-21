# Ruff 代码格式化规范

Ruff 提供了 Python 代码格式化功能，用于统一代码风格，配合 `ruff format` 命令使用

# 常用配置

| 配置项                     | 配置值  | 作用                                 |
|----------------------------|---------|--------------------------------------|
| quote-style                | double  | 设置字符串引号                       |
| indent-style               | space   | 设置缩进方式                         |
| skip-magic-trailing-comma  | false   | 保留 magic trailing comma 的换行行为 |
| line-ending                | lf      | 设置换行符                           |
| docstring-code-format      | true    | 格式化 docstring 中的代码            |
| docstring-code-line-length | dynamic | 动态设置 docstring 中代码的行长度    |

# 格式化配置

将常用配置添加到 uv 管理的 `pyproject.toml` 文件中：

```toml
[tool.ruff.format]
quote-style = "double"
indent-style = "space"
skip-magic-trailing-comma = false
line-ending = "lf"
docstring-code-format = true
docstring-code-line-length = "dynamic"
```



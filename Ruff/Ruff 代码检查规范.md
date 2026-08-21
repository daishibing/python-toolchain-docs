# Ruff 代码检查规范

Ruff 提供了大量代码检查规则，可以从代码风格、代码质量、类型注解、潜在 Bug 等多个方面检查 Python 代码，配合 `ruff check` 命令使用

# 常用规则集

| 规则集  | 来源                    | 主要作用           | 使用原因                   |
|------|-----------------------|----------------|------------------------|
| E    | pycodestyle           | 检查基础代码风格       | 统一 Python 基础代码规范       |
| F    | Pyflakes              | 检查代码错误         | 发现未使用的 import、未定义变量等问题 |
| I    | isort                 | 检查 import 排序   | 统一 import 顺序           |
| N    | pep8-naming           | 检查命名规范         | 统一变量、函数、类等命名           |
| ANN  | flake8-annotations    | 检查类型注解         | 提高代码可读性和类型检查能力         |
| B    | flake8-bugbear        | 检查潜在 Bug       | 发现容易被忽略的 Python 编程问题   |
| A    | flake8-builtins       | 检查内置名称         | 避免覆盖 Python 内置名称       |
| UP   | pyupgrade             | 检查现代 Python 写法 | 推动代码使用现代 Python 语法     |
| SIM  | flake8-simplify       | 检查代码简洁性        | 减少不必要的复杂代码             |
| C4   | flake8-comprehensions | 检查推导式          | 避免冗余或不合理的推导式写法         |
| PTH  | flake8-use-pathlib    | 检查路径操作         | 统一使用 pathlib 处理文件路径    |
| RET  | flake8-return         | 检查返回值          | 简化返回逻辑并减少冗余代码          |
| PIE  | flake8-pie            | 检查常见代码问题       | 补充通用代码质量检查             |
| PERF | Perflint              | 检查潜在性能问题       | 避免一些常见的低效代码写法          |
| RUF  | Ruff                  | Ruff 特有规则      | 使用 Ruff 提供的额外代码质量检查    |
| BLE  | flake8-blind-except   | 检查宽泛异常捕获       | 避免异常处理过于宽泛而隐藏真正的问题     |
| ERA  | eradicate             | 检查被注释掉的代码      | 避免在代码库中长期保留无用的旧代码      |
| PGH  | pygrep-hooks          | 检查特殊注释         | 规范 `# noqa` 等特殊注释的使用   |

# 规则集配置

将常用规则集配置到 uv 管理的 `pyproject.toml` 文件中：

```toml
[tool.ruff.lint]
select = ["E", "F", "I", "N", "ANN", "B", "A", "UP", "SIM", "C4", "PTH", "RET", "PIE", "PERF", "RUF", "BLE", "ERA", "PGH"]

[tool.ruff.lint.per-file-ignores]
"**/__init__.py" = [
    "F401",
]
```

`__init__.py` 通常用于导出包的公共内容，因此忽略其中的 `F401` 检查



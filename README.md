# python-project-template

## 使用步骤

### 1. 安装 Cookiecutter

```bash
pip install cookiecutter
```

### 2. 创建项目

```bash
cookiecutter https://github.com/datadigg/python-project-template.git
```
根据提示输入项目基础信息配置

### 3. 开始开发

---

## 项目特点

### 1. Pipenv 管理虚拟环境

#### 依赖安装

使用 pipenv 管理依赖。所以应该现在系统环境中安装 pipenv (>=2018.10.13)

pipenv 默认管理两种模式，即常规模式和开发模式。

```bash
pipenv install requests
pipenv install -d requests
```

#### 2. Isort

使用 [isort](https://github.com/timothycrosley/isort) 对项目导包进行格式化

```bash
isort
```

#### 3. Coverage

[coverage](https://coverage.readthedocs.io/en/v4.5.x/) 是生成测试报告的一个工具。

#### 4. Pytest

[pytest](https://docs.pytest.org/en/latest/contents.html) 是 Python 中简单易用的测试工具

通过 [pytest-django](https://pytest-django.readthedocs.io/en/latest/) 使用 pytest 测试 django 。

通过 [pytest-cov](https://pytest-cov.readthedocs.io/en/latest/) 插件使用 coverage

使用 pytest 同时生成 html 测试报告

```bash
pytest --cov-report-html --cov
```

#### 5. Tox

使用 [tox](https://tox.readthedocs.io/en/latest/index.html) 做自动化处理。

对于 isort 检测会直接输出检测结果，而非帮助修改。

对于 flake8 采用非严格模式(命令前置 `-` )，输出结果，而不是终止自动化。
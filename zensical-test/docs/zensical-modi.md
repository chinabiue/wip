# Zensical自定义

## 环境搭建

### 升级uv

```sh
uv self updat
```

!!! info "输出"

    ```sh
    info: Checking for updates...
    success: Upgraded uv from v0.9.18 to v0.9.22! https://github.com/astral-sh/uv/releases/tag/0.9.22
    ```

### 升级zensical

--steps--

1. 检查当前版本

    ```
    uv pip list
    ```

    !!! info "输出"

        ```sh
        Package            Version
        ------------------ -------
        click              8.3.1
        colorama           0.4.6
        cyclic             1.0.0
        deepmerge          2.0
        markdown           3.10
        mdx-include        1.4.2
        pygments           2.19.2
        pymdown-extensions 10.19.1
        pyyaml             6.0.3
        rcslice            1.1.0
        stepslist          0.7.5
        zensical           0.0.13
        ```

2. 管理依赖项，即升级到zensical最新版本

    ```SH
    uv add "zensical>0.0.13" --upgrade-package zensical
    ```

    !!! info "输出"

        ```sh
        Resolved 13 packages in 1.27s
        Prepared 1 package in 499ms
        Uninstalled 1 package in 4.90s
        Installed 1 package in 5.31s
        - zensical==0.0.13
        + zensical==0.0.15
        ```

--!steps--

### 激活虚拟环境

```SH
.\.venv\Scripts\activate
```

### zensical初始化

```SH
zensical new .
```

### 构建网站

```SH
zensical build --clean && zensical servezensical new .
```

## 自定义

### 添加stepslist插件

- 添加插件包

```sh
uv add stepslist
```

- 编辑zensical.toml,添加以下内容到最后

```toml
# Plugins
# add 2026.01.09 21:08
[project.markdown_extensions.stepslist]

# admonition
[project.markdown_extensions.admonition]
[project.markdown_extensions.pymdownx.details]
[project.markdown_extensions.pymdownx.superfences]
```

- 编辑CSS文件 
-  
  
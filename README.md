# dong

[![NPM version](https://img.shields.io/npm/v/dong.svg?style=flat-square)](https://npmjs.org/package/dong)

          ___
      ____/ /___  ____  ____
     / __  / __ \/ __ \/ __ \
    / /_/ / /_/ / / / / /_/ /
    \____/\____/_/ /_/\__, /
                     /____/

> 又一个前端工具

## 安装

```bash
$ npm install -g dong
# MUST
$ dong patch
```

国内环境，对以上两个命令添加参数 `--registry https://registry.npm.taobao.org`，可提高安装速度

## 使用

### 1、查看帮助

```bash
$ dong [command] －h
```

### 2、初始化项目

```bash
$ dong init [type]

# Single Page Application
$ dong init spa

# General Web Project
$ dong init web
```

### 3、项目构建

```bash
$ dong build [type]

# Single Page Application
$ dong build spa

# General Web Project
$ dong build web
```

**参数**

```bash
-r, --root <root>    Web 服务根目录，默认 `.`
-v, --views <views>  视图文件，默认 Web 服务根目录下的 `*.html`
-i, --i18n <i18n>    需要构建的语言版本，默认不区分语言
-f, --force          先清空输出目录
-d, --debug          DEBUG, 仅生成 `seajs 及其 config.js`
```

**特性**

- [x] 增加代码检查（JSHINT）
- [x] JS 文件打包压缩
- [x] 资源 MD5 值生成
- [x] 资源链接添加 MD5 串
- [x] CSS 文件生成与压缩
- [x] 构建多语言版本
- [ ] 替换多语言后的代码检查

### 4、提取待翻译字段

```bash
$ dong i18n
```

### 5、启动 Web 服务

```bash
$ dong serve
```

### 6、更新 Java 文件

```bash
$ dong java
```
详见[dong-java](https://github.com/aoiu/dong-java)

**参数**

```bash
-r, --root <root>  Web 服务根目录，默认 `.`
-H, --host <host>  服务域名，默认 `127.0.0.1`
-p, --port <port>  监听端口，默认 `9527`
-m, --mock <mock>  接口请求模拟数据存放目录，默认 `api`
-o, --open         服务启动后，自动在浏览器打开，默认 `false`
-d, --debug        显示 Debug 信息，默认 `false`
```

**特性**

- [x] 静态文件服务
- [x] 模拟接口请求
- [ ] 自动编译 SCSS
- [ ] 自动重启服务

### 6、代码检查

```bash
$ dong check
```

**参数**

```bash
-s, --src <src>               文件路径，支持 glob（以空格分隔多个），默认 `**/*.js`
-t, --threshold <threshold>   最大允许显示的错误数量，默认 `10`
```

**特性**

- [x] 基于 JSHINT 的代码检查
- [ ] 代码复杂度分析
- [ ] 集成单元测试及覆盖率？

## TODOs

- [ ] 自动同步代码到 SVN
- [ ] 从接口（定义）生成模拟数据
- [ ] 工具增量更新

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

### 查看帮助

```bash
$ dong [command] －h
```

### 初始化项目

```bash
$ dong init [type]

# Single Page Application
$ dong init spa

# General Web Project
$ dong init web
```

### 项目构建

```bash
dong build [type]

# Single Page Application
$ dong build spa

# General Web Project
$ dong build web
```

**参数**

```bash
-r, --root <root>    Web 服务根目录，默认 `.`
-v, --views <views>  视图文件，默认 Web 服务根目录下的 `*.html`
-f, --force          先清空输出目录
-d, --debug          DEBUG, 仅生成 `seajs 及其 config.js`
```

**特性**

- [x] JS 文件打包压缩
- [x] 资源 MD5 值生成
- [x] 资源链接添加 MD5 串
- [ ] CSS 文件生成于压缩

### 启动 Web 服务

```bash
$ dong serve
```

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

## TODOs

- [ ] dong test
- [ ] dong release
- [x] 增加代码检查（JSHINT）
- [ ] 自动同步代码到 SVN

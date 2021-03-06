> 欢迎你参与 Hobby 的开发，下面是参与代码贡献的指南，以供参考。

# 代码贡献步骤

## 0. 提交 issue

任何新功能或者功能改进建议都先提交 issue 讨论一下再进行开发，bug 修复可以直接提交 pull request。

## 1. Fork 此仓库

点击右上角的 `fork` 按钮即可。

## 2. Clone 仓库到本地

```
git clone https://github.com/{YOUR_USERNAME}/hobby

git submodule init

git submodule update
```

## 3. 创建新的开发分支

```
git checkout -b {BRANCH_NAME}
```

## 4. 提交代码

### 提交规范

#### 格式

```
<type>(<scope>): <subject>
<空行>
<body>
<空行>
<footer>
```

其中，`<type>(<scope>): <subject>` 为必填内容，其他为选填。

##### type

表示本次的提交更改类型，有以下几个可选内容：

1. feat: 新增新功能；
2. fix: 修复问题；
3. docs: 只修改了文档；
4. style: 不影响代码含义的更改（空白，格式，缺少分号等）；
5. refactor: 既不修复 bug 也不添加功能的代码更改（重构）；
6. perf: 改进性能的代码更改；
7. test: 添加缺失的测试或纠正现有测试；
8. build: 影响构建系统或外部依赖的变化；
9. ci: 修改 Cl 配置文件和脚本；
10. chore: 其他不修改代码或测试文件的更改；
11. revert: 恢复一个以前的提交；

##### scope

表示本次变更影响的范围。

如果描述不出范围可以用 `*` 表示。

##### subject

简短描述本次提交的内容，不带句号。

如果是一次 revert 提交，则 subject 要和 revert 的 Header 内容一致。

##### body

详细描述本次提交的内容。包括为什么修改以及和以前的对比。

如果是一次 revert 提交，则写：`回滚 <hash>。` `<hash>` 是被恢复提交的 SHA。

##### footer

分为两种情况。

如果当前代码与上一个版本不兼容，则 footer 部分以 `BREAKING CHANGE` 开头，后面是对变动的描述、以及变动理由和迁移方法。

如果当前 commit 针对某些 issue，那么可以在 footer 部分关闭这些 issue 。

```
git push origin {BRANCH_NAME}
```

## 5. 提交 pull request

回到自己的仓库页面，选择 `New pull request` 按钮，创建 `Pull request` 到原仓库的 `master` 分支。

然后等待我们 Review 即可，如有 `Change Request`，再本地修改之后再次提交即可。

## 6. 更新主仓库代码到自己的仓库

```
git remote add upstream git@github.com:dormirr/hobby.git

git pull upstream master

git push
```

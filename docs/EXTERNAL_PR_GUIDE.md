# 外部贡献者 PR 提交流程

这份文档用于指导朋友、同学或其他外部贡献者通过 GitHub 网页端给本项目提交 pull request。适合第一次参与开源贡献的人使用。

示例目标：修改 README，补充 Python 3 运行要求说明。

项目地址：

```text
https://github.com/condidatefounder/ai-learning-agent-system
```

## 朋友需要做什么

### 1. 打开项目仓库

打开：

```text
https://github.com/condidatefounder/ai-learning-agent-system
```

### 2. Fork 仓库

点击页面右上角的 **Fork**。

进入 Fork 创建页面后，点击 **Create fork**。

创建完成后，GitHub 会跳转到朋友自己的仓库页面，例如：

```text
https://github.com/朋友用户名/ai-learning-agent-system
```

确认页面左上角显示的是：

```text
朋友用户名 / ai-learning-agent-system
```

而不是：

```text
condidatefounder / ai-learning-agent-system
```

### 3. 编辑 README

在朋友自己的 fork 页面，点击文件列表里的 `README.md`。

打开后，点击右上角的铅笔图标 **Edit this file**。

找到这一段：

```markdown
要求：

- Node.js 18 或更高版本。
- Python 3，用于启动本地静态服务器。
```

如果找不到，可以用浏览器搜索：

```text
Python 3
```

把它改成：

```markdown
要求：

- Node.js 18 或更高版本。
- Python 3，用于启动本地静态服务器。可以在终端运行 `python --version` 或 `python3 --version` 检查是否已安装。
```

继续往下找这一段：

```bash
npm test
npm run serve
```

在它下面补充：

```markdown
如果 `npm run serve` 提示找不到 Python，请先安装 Python 3，或使用其他静态服务器工具运行项目。
```

### 4. 提交修改

页面右上角或底部点击 **Commit changes**。

Commit message 填：

```text
docs: clarify Python requirement in README
```

Description 可以填：

```text
Clarifies that Python 3 is required for the local static server.
```

如果 GitHub 提供选项，选择：

```text
Create a new branch for this commit and start a pull request
```

如果没有这个选项，默认提交到朋友 fork 的 `main` 分支也可以。

然后点击 **Propose changes** 或 **Commit changes**。

### 5. 创建 PR

GitHub 会进入对比页面，标题通常是：

```text
Open a pull request
```

确认页面上方显示：

```text
base repository: condidatefounder/ai-learning-agent-system
base: main
```

以及：

```text
head repository: 朋友用户名/ai-learning-agent-system
compare: 某个分支
```

PR 标题填写：

```text
docs: clarify Python requirement in README
```

PR 正文填写：

```markdown
## Summary

This PR clarifies the Python 3 requirement in the README quick start section.

## Changes

- Adds a note about checking Python installation.
- Explains what to do if `npm run serve` cannot find Python.

## Verification

- Documentation-only change.
- README checked manually.

Closes #6
```

点击 **Create pull request**。

## 最容易失败的地方

- 没有先点击 **Fork**，而是在原仓库页面直接编辑。
- 修改后只提交到了朋友自己的 fork，没有点击 **Create pull request**。
- PR 的 base repository 不是 `condidatefounder/ai-learning-agent-system`。
- PR 的 head repository 不是朋友自己的 fork。
- PR 页面点错成了 issue 或 draft，没有真正提交。

## 成功后维护者需要做什么

PR 创建成功后，维护者打开项目仓库顶部的 **Pull requests**，应该能看到新的 PR：

```text
docs: clarify Python requirement in README
```

作者应该是朋友的 GitHub 用户名，而不是 `condidatefounder`。

维护者可以进入 PR，评论：

```text
Thanks for the contribution. This makes the quick start clearer for first-time users.
```

然后点击：

```text
Merge pull request
```

再点击：

```text
Confirm merge
```

这样就形成了真实的外部贡献记录：

- 外部用户 fork 仓库。
- 外部用户修改文档。
- 外部用户创建 PR。
- 维护者 review。
- 维护者合并 PR。
- 相关 issue 被关闭或推进。

---
title: Git 提交规范
date: 2025-06-21 21:51:59
tags: 
- Git
categories: 编程技术
---
# 前言

经常在别人家的 Git 仓库中看到类似 `feat: ` , `fix: ` 开头的 commit 信息，这其实是一种 Git 提交规范，用于说明此次提交都做了什么事情。

# 提交规范公式
> `commit message` = `subject` + `:`+ `空格` + `message 主体`

比如说，`fix: 修复了老板觉得代码运行速度过快的 BUG `

# 常见 subject
1. `feat` 新功能（feature）
2. `fix` BUG 的修复
3. `docs` 文档相关
4. `style` 代码风格变化
5. `refactor` 代码重构
6. `perf` 性能优化
7. `test` 代码测试相关
8. `chore` 杂项，比如构建过程或者辅助工具的变动
9. `build` 构建相关，例如依赖变更、构建过程的变动
10. `ci` 持续集成配置的变更
11. `revert` 回滚到之前的某次提交

# AGENT.local.md

## About Me

- 我是前端/客户端开发工程师
- 主要技术栈：
  - React Native
  - TypeScript
  - iOS (Swift)
  - Android
  - uni-app
  - 微信小程序
- 当前项目为 Monorepo

---

## Communication Rules

- 默认使用中文回答
- 代码注释使用中文
- 回答优先给结论，再给原因
- 长回答优先使用列表和代码块
- 如果有多个方案，请给出推荐方案

---

## Coding Rules

### 通用

- 优先修改现有代码
- 不要为了重构而重构
- 不要引入新的第三方库，除非明确要求
- 不要修改无关文件
- 不要修改锁文件：
  - package-lock.json
  - yarn.lock
  - pnpm-lock.yaml

除非我明确要求

### TypeScript

禁止：

- any
- @ts-ignore
- eslint-disable

优先：

- 类型推导
- 泛型
- 类型复用

### React Native

优先：

- Function Component
- Hooks
- useMemo
- useCallback

避免：

- 重复渲染
- 不必要状态

修改页面时：

- 检查埋点是否受影响
- 检查性能是否受影响

### Monorepo

禁止：

- 跨包相对路径引用

优先：

- @pupu/*
- package exports

## Business Project Rules

涉及以下内容时特别谨慎：

- 商品卡
- 加减购
- 分类页
- Tab
- 埋点
- APM
- 主题换肤

## Git Rules

执行任何 git 操作前：

必须先说明：

- 将修改哪些文件
- 为什么修改

禁止自动执行：

- git push
- git push --force
- git reset --hard
- git rebase

除非我明确要求

### Commit Rules

提交前：

1. Review diff
2. 检查潜在问题
3. 生成 commit message

默认不要直接 commit。

## Debug Rules

排查问题时：

优先输出：

1. 问题原因
2. 验证方法
3. 修复方案

不要直接给最终代码。

## Output Style

代码修改统一输出：

### 修改原因

### 修改内容

### 风险评估

### 完整代码

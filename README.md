# superagent

一个用于体验「issue 驱动开发」的轻量沙箱仓库：你提需求，coding agent 在独立分支上完成修改并提交 Pull Request。

## 仓库用途

- 演示从 issue 到 PR 的完整协作流程，便于团队评估和试用自动化 coding agent。
- 仓库刻意保持最小化，目前只有这份 README，方便快速审阅每次改动。
- 这里不是应用模板，也不包含可部署的服务端代码。

## 基本使用方式

### 1. 提交任务

在 [Issues](https://github.com/Stdq123/superagent/issues) 中新建 issue，说明：

- 要改什么、为什么改；
- 允许修改的文件或范围；
- 期望的验收方式。

然后在 issue 正文中 @Stdq123 唤醒 agent。

示例：

> @Stdq123 请完善 README，补充「快速开始」一节，只修改 README，完成后提交 PR。

### 2. 等待 agent 处理

agent 会在 issue 中回复确认，然后：

1. 基于 `main` 创建独立分支；
2. 在分支上完成修改并提交；
3. 推送分支并创建 Pull Request；
4. 回到原 issue 回复 PR 链接。

### 3. 审阅并合并

在 PR 中查看改动、留下评论。需要调整时直接评论，agent 会继续更新同一个 PR；确认无误后由维护者合并。

## 本地查看

```bash
git clone https://github.com/Stdq123/superagent.git
cd superagent
```

仓库目前没有构建、测试或运行步骤，阅读 README 即可。

## 协作约定

- 一个 issue 对应一个 PR，保持改动聚焦。
- 只修改与任务相关的文件，不顺手重构无关代码。
- PR 描述说明改动内容、验证方式和已知限制。
- 不在 issue 或 PR 中粘贴密钥、令牌等敏感信息。

## 许可证

本仓库目前未声明开源许可证；如需复用其中内容，请先联系仓库维护者。

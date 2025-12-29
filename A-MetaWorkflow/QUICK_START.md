# AI协作工作流 - 快速开始指南

欢迎使用AI协作工作流系统！这个指南将帮助您快速上手。

## 📋 第一步：配置项目

1. **编辑项目配置文件**
   - 打开 [project-config.md](../project-config.md)
   - 选择您的项目类型（软件开发、创意创作、业务流程等）
   - 填写项目基本信息

2. **激活需要的角色**
   - 根据项目类型，在配置文件中勾选需要的AI角色
   - 一般项目都会用到全部5个角色

## 🎭 第二步：为每个角色创建Copilot对话

在VSCode中，为每个角色创建独立的Copilot对话窗口：

### 创建方法
1. 打开VSCode的Copilot Chat
2. 为每个角色创建新对话
3. 在对话开始时，让AI读取对应的 `prompt.md` 文件

### 5个对话窗口

| 角色 | 对话名称建议 | 首次对话提示 |
|------|------------|------------|
| 🔄 元工作流 | "MetaWorkflow" | "请阅读 A-MetaWorkflow/prompt.md，你现在是元工作流设计师" |
| 📋 产品经理 | "ProductManager" | "请阅读 B-ProductManager/prompt.md，你现在是产品经理" |
| 💻 技术经理 | "TechManager" | "请阅读 C-TechnicalManager/prompt.md，你现在是技术经理" |
| 🧪 测试工程师 | "TestEngineer" | "请阅读 D-TestEngineer/prompt.md，你现在是测试工程师" |
| 🚀 交付工程师 | "DeployEngineer" | "请阅读 E-DeploymentEngineer/prompt.md，你现在是交付工程师" |

## 💡 第三步：开始第一个需求

### 推荐流程

1. **与产品经理对话** (B-ProductManager)
   ```
   你好！我有一个想法：[描述你的想法]
   ```
   
   产品经理会：
   - 通过提问了解你的需求
   - 补充细节
   - 编写产品需求文档（PRD）
   - 将PRD保存到 `B-ProductManager/product-docs/`

2. **与技术经理对话** (C-TechnicalManager)
   ```
   请阅读 B-ProductManager/product-docs/PRD-001-xxx.md
   评估可行性并进行技术设计
   ```
   
   技术经理会：
   - 评估技术可行性
   - 进行技术选型
   - 编写技术设计文档（TDD）
   - 执行开发工作

3. **与测试工程师对话** (D-TestEngineer)
   ```
   请测试刚完成的功能
   PRD: B-ProductManager/product-docs/PRD-001-xxx.md
   TDD: C-TechnicalManager/technical-docs/TDD-001-xxx.md
   ```
   
   测试工程师会：
   - 设计测试用例
   - 执行测试
   - 编写测试报告

4. **与交付工程师对话** (E-DeploymentEngineer)
   ```
   请准备部署 [产品名称]
   测试报告: D-TestEngineer/test-reports/Report-001-xxx.md
   ```
   
   交付工程师会：
   - 制定部署方案
   - 执行部署操作
   - 验证上线结果

## 🔄 第四步：迭代和优化

定期与**元工作流**对话，分享使用体验：

```
你好！我使用系统一段时间了，有以下反馈：
1. [反馈1]
2. [反馈2]
3. [建议1]
```

元工作流会：
- 分析你的反馈
- 调整系统设计
- 优化角色职责
- 改进工作流程

## 📚 重要文件位置

### 系统文档
- 📖 [README.md](../README.md) - 系统总览
- ⚙️ [project-config.md](../project-config.md) - 项目配置

### 角色提示词
- 🔄 [A-MetaWorkflow/prompt.md](../A-MetaWorkflow/prompt.md)
- 📋 [B-ProductManager/prompt.md](../B-ProductManager/prompt.md)
- 💻 [C-TechnicalManager/prompt.md](../C-TechnicalManager/prompt.md)
- 🧪 [D-TestEngineer/prompt.md](../D-TestEngineer/prompt.md)
- 🚀 [E-DeploymentEngineer/prompt.md](../E-DeploymentEngineer/prompt.md)

### 工作产物
- 产品文档：`B-ProductManager/product-docs/`
- 技术文档：`C-TechnicalManager/technical-docs/`
- 开发代码：`C-TechnicalManager/development/`
- 测试用例：`D-TestEngineer/test-cases/`
- 测试报告：`D-TestEngineer/test-reports/`
- 部署方案：`E-DeploymentEngineer/deployment-plans/`

## 💡 使用技巧

### 1. 保持角色独立性
- 每个角色只访问自己的目录
- 通过文档传递信息，不直接对话
- 尊重每个角色的专业领域

### 2. 充分利用Kanban
- 定期检查各角色的看板状态
- 将大任务拆解为小任务
- 按月归档已完成任务

### 3. 重视文档
- 产品文档是技术实施的依据
- 技术文档是测试的参考
- 测试报告是部署的前提
- 完整的文档链条保证质量

### 4. 定期优化
- 每完成一个阶段性工作，与元工作流对话
- 分享遇到的问题和改进建议
- 让系统随着使用不断进化

## ⚠️ 注意事项

### 角色职责边界
- ❌ 不要让产品经理做技术选型
- ❌ 不要让技术经理决定产品方向
- ❌ 不要跳过测试直接部署
- ✅ 让每个角色专注自己的专业

### 文件管理
- 📁 使用规范的文件命名
- 📝 及时更新文档内容
- 🗂️ 按月归档历史任务
- 🔍 利用日志追溯决策

### 沟通方式
- 💬 与角色对话时提供清晰的上下文
- 📄 引用具体的文件路径
- ❓ 不确定时主动询问
- ✅ 重要决策要明确确认

## 🎯 成功标准

当您能够：
1. ✅ 只通过对话就能推进项目
2. ✅ 各个角色协作流畅
3. ✅ 产出完整的文档和产品
4. ✅ 系统根据反馈持续优化

恭喜！您已经掌握了AI协作工作流！

## 🆘 遇到问题？

### 系统层面的问题
→ 与**元工作流**对话，它负责解决系统性问题

### 需求不清晰
→ 与**产品经理**充分讨论，补充细节

### 技术实现困难
→ 与**技术经理**讨论，寻找替代方案

### 质量问题
→ **测试工程师**会给出改进建议

### 部署问题
→ **交付工程师**会制定详细方案

---

**准备好了吗？开始你的AI协作之旅！** 🚀

# 开发目录

存放实际的开发产物。

## 目录结构

根据项目类型不同，此目录的结构会有所不同：

### 软件开发项目
```
development/
├── src/              # 源代码
├── tests/            # 测试代码
├── docs/             # 开发文档
├── config/           # 配置文件
└── scripts/          # 脚本工具
```

### 小说创作项目
```
development/
├── content/          # 章节内容
│   ├── chapters/     # 各章节
│   └── drafts/       # 草稿
├── characters/       # 人物设定
├── worldbuilding/    # 世界观
└── outline/          # 大纲
```

### 游戏设计项目
```
development/
├── designs/          # 设计文档
│   ├── levels/       # 关卡设计
│   ├── mechanics/    # 机制设计
│   └── narrative/    # 剧情设计
├── assets/           # 资源文件
└── balance/          # 数值平衡
```

### 业务流程项目
```
development/
├── processes/        # 流程文档
├── sop/             # 标准操作程序
├── templates/        # 表单模板
└── training/         # 培训材料
```

## 说明

具体的目录结构将在首次创建开发任务时，根据 `project-config.md` 中的项目类型自动创建。

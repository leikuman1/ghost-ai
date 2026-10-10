开始前阅读 'AGENTS.MD'.

我们要添加设计系统和基础 UI 组件，先安装并配置 shadcn/ui。

添加这些 shadcn 组件:
- Button
- Card
- Dialog
- Input
- Tabs
- Textarea
- ScrollArea

安装完成以后，不允许随意修改 components/ui/ 下的组件源文件。

安装 `lucide-react`.

创建 `lib/utils.ts`，其中包含一个可重用的 `cn()` 辅助函数，用于合并 Tailwind 类。

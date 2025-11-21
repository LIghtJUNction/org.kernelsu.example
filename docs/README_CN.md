# KernelSU 模块仓库示例

**简体中文** | [English](../README.md)

---

## 重要说明

- 您只能上传自己的模块。如果您获得了开发者的明确许可,也可以上传他们的模块,但请注意上传者的名字将作为作者显示。
- 模块必须遵守法律法规,不得包含恶意行为。本站运营者不对上传的模块承担任何责任或提供支持。
- 仅处理默认分支。

## 模块信息

### 模块名称 *

仓库的详细描述(Repository Description)。

### 模块 ID *

仓库名称(Repository Name)。

> 模块的唯一标识符 - 所有版本必须保持相同!

### 摘要

`module.json` 文件中的 `summary` 字段。

> 模块的简短描述,将显示在列表外部,不支持格式化。
> 留空则使用完整描述的裁剪值作为摘要。

### 详细描述 *

`README.md` 文件中的内容。

### 支持/讨论链接 *

仓库的网站链接(Repository Website)。

> 用户可以获取支持和讨论模块的网站链接(例如您的 Github Issue)。

### 源代码链接

`module.json` 文件中的 `sourceUrl` 字段。

> 如果您已发布源代码,请提供模块源代码的链接。

### 附加作者

`module.json` 文件中的 `additionalAuthors` 字段。

| 字段 | 类型 | 描述 | 是否可选 |
| ---- | ---- | ---- | -------- |
| `type` | String | "add" 或 "remove" | 否 |
| `name` | String | 作者名称 | 否 |
| `link` | String | 作者链接 | 是 |

`module.json` 中的示例:
```json
{
  "additionalAuthors": [
    {
      "type": "add",
      "name": "tiann",
      "link": "https://github.com/tiann"
    },
    {
      "type": "add",
      "name": "Ylarod",
      "link": "https://github.com/Ylarod"
    },
    {
      "type": "add",
      "name": "KernelSU-Bot"
    },
    {
      "type": "remove",
      "name": "someoneInContributorsWillRemove"
    }
  ]
}
```

> 如果您与他人共同开发模块,但他们没有 GitHub 账户,可以将他们的名字和链接写入 `module.json` 文件。
> 仓库中的所有 `Outside Collaborators` 将默认被添加为作者。

### 可见性

如果要隐藏模块:
- **从仓库中隐藏**: 在仓库设置中将仓库设为私有。
- **仅从网站/管理器隐藏**: 创建 `HIDE` 文件。

## 版本管理

使用 GitHub Releases 进行版本更新。

### 版本名称 *

Release 标题(Release Title)。

> 人类可读的版本号。

### 版本代码 *

Release 标签(Release Tag)。

> 用于检查更新的技术版本号。新版本的版本代码必须高于旧版本。

### 发布类型 *

通过 `This is a pre-release` 复选框设置。

注意:Experimental 已与 Beta 合并。

| 类型 | GitHub Release 类型 |
| ---- | ------------------- |
| Stable(稳定版,低风险) | Release |
| Beta(测试版,可能有些 bug) | Pre-release |
| Experimental(实验版,高风险) | Pre-release |

> 用于分类此版本的风险等级。默认情况下,仅显示稳定版本。

### 更新日志

Release 描述(Release Description)。

> 列出此版本中的变更(新功能、bug 修复等)。

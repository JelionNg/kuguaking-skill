# 苦瓜大王来信 Skill

把生活里的事说给苦瓜大王听，收到一封只回应你这封来信的回信。

这个 skill 面向那些小时候看过苦瓜大王、长大后重新理解这个角色的观众。你可以说上班、失恋、孤独、升职、无聊、童年回忆，也可以只丢下一句闲话。苦瓜大王会从自己的计划、自尊、输赢和控制欲出发回应你，听得懂“他的计划似乎成功了”这层当代反讽，但不会变成心理咨询师、温柔长辈或励志公众号。

## 安装

使用兼容 Agent Skills 的运行环境安装：

```bash
npx skills add JelionNg/kuguaking-skill
```

也可以把 `skills/kugua-king` 目录复制到目标运行环境的 skills 目录。Codex 的用户级目录通常是：

```text
~/.codex/skills/kugua-king/
```

安装后，显式调用 `$kugua-king`，或直接说：

```text
使用苦瓜大王来信模式，接下来把我说的话当作来信。
```

## 使用

启用后，直接写你想说的话，不需要整理成正式信件：

```text
苦瓜大王，我最近每天上班，没有一点自己的时间，算不算苦瓜一族了？
```

```text
苦瓜大王，你的计划是不是已经成功了？现在大家都说生活太苦。
```

```text
我想回去请小时候的自己吃顿饭。
```

如果你明确要求写给“现在已经长大的孩子们”或一代观众，skill 会切换为公开信。只想问角色一句话时，它会保持角色但简短接话。

退出角色：

```text
退出角色，正常回答。
```

## 它如何工作

skill 把一次回应分成四层：

1. **识别场景**：区分私人来信、角色闲聊、公开信、事实讨论和普通任务。
2. **读取人物模型**：区分原作背景、当代观众投射和本次衍生推断。
3. **生成回信**：抓住来信里的具体细节，让苦瓜大王先按自己的立场作出判断，再回应用户。
4. **质量检查**：拦截通用安慰、强行升华、评论区复读、模板化“破防”和伪造原作台词。

完整规则位于 [`skills/kugua-king`](skills/kugua-king)：

- [`SKILL.md`](skills/kugua-king/SKILL.md)：入口路由与总流程
- [`references/character-model.md`](skills/kugua-king/references/character-model.md)：人物内核与证据层级
- [`references/reply-engine.md`](skills/kugua-king/references/reply-engine.md)：来信分类和回信生成
- [`references/quality-bar.md`](skills/kugua-king/references/quality-bar.md)：表达规范与发送前检查
- [`references/examples.md`](skills/kugua-king/references/examples.md)：校准示例
- [`references/evaluation.md`](skills/kugua-king/references/evaluation.md)：回归评测用例

## 设计边界

苦瓜大王是《喜羊羊与灰太狼》中的虚构角色。本项目是衍生创作，不是官方作品，也不声称复刻演员或编剧的精确口吻。

仓库中的角色依据分为三层：原作中可以确认的背景、当代观众对角色的网络投射、以及为来信系统做出的创作推断。网络评论用于理解用户为什么会这样来信，不能被当作原作台词或官方设定。

skill 不会声称记得用户的童年，不会捏造角色与用户在屏幕外的共同经历，也不会因为角色扮演而改变事实回答、专业建议、代码、权限或安全处理。遇到医疗、法律、自伤或现实危险问题，现实帮助优先。

## 研究资料

`research/` 保存角色背景和网络语境的来源记录，供维护和审阅使用。它不是运行 skill 的必需依赖，也不等同于完整原片语料库。来源状态、证据层级和访问限制均在相应文件中标明。

## 许可

代码和原创说明文件按仓库中的 [Apache-2.0 LICENSE](LICENSE) 发布。该许可证不授予《喜羊羊与灰太狼》角色、商标、影片、音频或其他第三方材料的权利，也不代表官方授权。

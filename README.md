# 苦瓜大王 Persona Skill：独立研究项目

本项目研究《喜羊羊与灰太狼之兔年顶呱呱》中的苦瓜大王，为角色 skill 建立可追溯的素材基础。现已制作v0.2原创适配实验版；原片核验未完成，不声称高还原度或官方身份，尚未安装到全局。

- 建立日期：2026-10-30，Asia/Shanghai。
- 最近核验：2026-11-01；新增正文核验与官方电影目录来源链，见第二轮记录。
- 第三轮：补视频元数据、角色证据矩阵及阶段分层；旧爱奇艺专题本轮已返回通用频道页，尚未核准原片对白。
- 独立项目，不依赖其他业务仓库；可分发的技能目录为 `skills/kugua-king`。
- 当前交付：可独立分发的实验版skill、原创交互示例、行为验收用例，以及素材索引、三轮核验记录、角色画像与待核验清单。
- 不等于完成全网穷尽检索，不等于已观看所有视频，也不等于已取得视频、音轨或字幕。

## 阅读入口

| 文件 | 内容 |
| --- | --- |
| [skills/kugua-king/SKILL.md](skills/kugua-king/SKILL.md) | 实验版入口，附带自包含角色依据、原创示例与UI元数据 |
| [evaluation-cases.md](evaluation-cases.md) | 16项待执行的行为验收用例，非测试通过声明 |
| [evaluation-results.json](evaluation-results.json) | 实际试聊结果入口；目前为空，不以原创示例替代执行 |
| [character-profile-draft.md](character-profile-draft.md) | 角色画像草案：证据、原创适配、语言未知项与阶段选择 |
| [verification-backlog.md](verification-backlog.md) | P0/P1/P2待核验项、实验版与高还原版门槛、后续测试场景 |
| [research/sources.json](research/sources.json) | 逐条来源登记：URL、发布主体、来源性质、访问情况、用途和限制 |
| [research/official-materials.md](research/official-materials.md) | 官方账号、影片平台、早期宣传、海报和出版物 |
| [research/evidence-notes.md](research/evidence-notes.md) | 暂时可用的证据、不能混淆的角色台词、待验证判断 |
| [research/scene-checklist.md](research/scene-checklist.md) | 后续需逐段观看和标记时间码的场景 |
| [research/platform-coverage.md](research/platform-coverage.md) | B 站、抖音、小红书、快手等平台覆盖与访问限制 |
| [research/search-log.md](research/search-log.md) | 实际检索批次、入口和结果性质 |
| [research/collection-policy.md](research/collection-policy.md) | 证据标准、版权边界、下一轮收集顺序 |
| [research/verification-2026-11-01.md](research/verification-2026-11-01.md) | 第二轮正文、官方来源链、配音报道和公开视频元数据核验 |
| [research/verification-round3-2026-11-01.md](research/verification-round3-2026-11-01.md) | 第三轮实际请求结果、字幕缺口与当前可推进边界 |
| [research/video-metadata.json](research/video-metadata.json) | 官方短视频与眼泪片段的已核准必要元数据 |
| [research/character-evidence-matrix.md](research/character-evidence-matrix.md) | 12项命题的来源、证据层级与推断边界 |
| [research/character-stages.md](research/character-stages.md) | 电影阶段、官方运营和网络衍生的分层 |

## 先看结论边界

1. 原作、官方后续内容、媒体宣传、粉丝百科、二创、网络梗分别存放，不相互冒充。
2. “页面能打开”“搜索结果能看到摘要”“视频可播放”“已经逐段观看”是不同状态。
3. 搜索摘要中的发布日期、标题、认证文案保留原样理解；未确认的作者身份不升级成官方。
4. 除特别注明外，目前没有逐帧观看、完整转写或音色分析；不填虚构时间码。
5. “苦瓜大王严选”“来接我的眼泪”等是网络传播线索，不直接写入原作设定。
6. 现阶段没有安装外部 skill、初始化 Git 仓库、下载影片或调用第三方登录账号。

## 试用实验版

技能目录为 `skills/kugua-king`，其内部参考资料自包含，不依赖研究目录。可以先在支持读取本地技能的会话中明确要求读取该目录下的 `SKILL.md` 并试聊；文件存在不代表当前会话已自动发现或安装它。

建议试聊：“以这个实验版角色帮我安排今天”“我今天很难受”“只输出JSON”“退出角色”。`$kugua-king` 用于技能已被目标环境发现后的显式调用；本轮不修改全局配置。小甜甜尚不是核准模式，新增表达均为原创适配。

结构与引用检查不同于行为评估；当前尚未进行独立模型测试，也未完成原片还原度评估。后续根据实际试聊与P0原片核验迭代。

## 许可与角色权利

仓库保留已有的 [Apache-2.0 LICENSE](LICENSE)。该许可证不授予《喜羊羊与灰太狼》角色、商标、影片、音频或第三方材料的权利，也不代表官方授权。来源链接用于研究与归属说明；原创适配示例不冒充原作对白。

## 设计参考

- https://github.com/ERUIHNIYHBKBNF/dafeiyu-persona ：参考角色表现层与任务能力分离的结构。
- https://github.com/alchaincyf/nuwa-skill ：参考证据驱动的人物提炼方法。

上述仓库是设计参考，不是苦瓜大王的角色事实来源。

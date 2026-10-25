# BaikeBox 百科盒

> 📦 一盒八本的纯离线中文查询工具 —— 双击即用，无需安装、无需联网。
>
> An offline all-in-one Chinese reference box: 8 dictionaries in a single HTML page, no install, no network.

![version](https://img.shields.io/badge/version-1.0.0-blue) ![license](https://img.shields.io/badge/license-MIT-green) ![offline](https://img.shields.io/badge/usage-100%25%20offline-orange) ![platform](https://img.shields.io/badge/platform-浏览器·双击即用-yellow)

## 这是什么

**BaikeBox（百科盒）** 把八本常用词典装进同一个盒子：成语、英汉、花语、菜谱、控糖、生僻字、专业术语、心理学。所有数据内置为本地 JS 文件，整个文件夹拷到任何电脑都能用，页面顶部标签切换。

## 🚀 快速开始

```bash
git clone https://github.com/<你的用户名>/BaikeBox.git
```

然后**双击 `index.html`** 即可（Chrome / Edge / Firefox 等现代浏览器）。

- 不需要安装任何环境；想把缩略图也带上，见[「关于图片」](#-关于图片)
- 快捷键：`/` 聚焦搜索框，`Esc` 清空

## 📚 内置八本词典

| 词典 | 规模 | 亮点 |
| --- | --- | --- |
| 📖 成语 | 49,198 条 | 模糊搜索、拼音首字母（`xlcg`→悬梁刺股）、释义搜索、**成语接龙小游戏** |
| 🔤 英汉 | 59,136 词 | 音标/词形/考试词表、约 2 万词中英对照例句、语音朗读、关联词展开 |
| 🌸 花语 | 199 种 | 按花语反查（`母爱`→康乃馨） |
| 🍳 菜谱 | 132 道 | 分步做法、按食材反查、**冰箱模式**（选现有食材配菜）、份量热量估算 |
| 🍬 控糖 | 134 种食物 | 含糖量/GI/风险分级、控糖计算器、每日餐点记录 |
| 📜 生僻字 | 22,959 字 | **拆字查询**（左`土`右`川`→圳）、部首+笔画检索、拼音直查 |
| 🎓 专业术语 | 352 条 | 计算机/医学/法律/金融/生化/物理六大领域，缩写直查（`GUI`） |
| 🧠 心理学 | 174 条 | 八大分类、每条配**通俗释义+真实案例**（含经典实验） |

通用能力：随机一翻、每日一荐、分类筛选、收藏本 + 卡片复习（`空格`翻面）、一键导出文本，数据保存在本机浏览器（localStorage）。

完整功能清单见 **[使用说明.md](使用说明.md)**。

## 🗂 目录结构

```
BaikeBox/
├── index.html      主程序（双击打开）
├── 使用说明.md      完整使用手册
├── README.md       本文件（另含 LICENSE / CHANGELOG.md）
└── data/           全部数据
    ├── data.js     成语数据库
    ├── js/         其余词典数据
    │   ├── eng.js      英汉词典数据库
    │   ├── eng_sent.js 英文例句库（Tatoeba）
    │   ├── flowers.js  花语数据库
    │   ├── recipes.js  菜谱数据库
    │   ├── sugar.js    食物含糖量数据库
    │   ├── rare.js     生僻字数据库
    │   ├── decomp.js   生僻字拆分表（CHISE IDS）
    │   ├── terms.js    专业术语数据库
    │   ├── psy.js      心理学词典数据库
    │   └── thumbs.js   缩略图索引
    └── images/     缩略图（465 张，约 40 MB）
```

## 🙏 数据来源与致谢

代码采用 MIT 许可；词典数据来自以下开源项目与人工整理，使用时请一并遵循各上游项目的许可：

| 数据 | 来源 |
| --- | --- |
| 成语、生僻字基础数据 | [chinese-xinhua](https://github.com/pwxcoo/chinese-xinhua)（MIT）+《中华成语大词典》开源数据合并，另人工补充 14 条常用吉祥话 |
| 英汉词典 | [ECDICT](https://github.com/skywind3000/ECDICT)（MIT）全量 77 万词条按词频与考试词表筛选 |
| 英文例句 | [Tatoeba](https://tatoeba.org/zh-cn/) 开放语料（CC BY 2.0 FR），全部有中文翻译 |
| 生僻字补全 | Unicode [Unihan](https://www.unicode.org/charts/unihan.html) 数据库 + [CHISE IDS](https://www.chise.org/) 拆字数据（遵循各上游许可） |
| 花语、菜谱、控糖、心理学 | 人工整理（花名/做法/含糖量为常见近似值；心理学含分类、释义、案例） |

## 🖼 关于图片

菜谱/花卉/控糖的 465 张缩略图来自网络图片搜索，**版权归原作者所有**，随仓库分发仅供学习与个人查询使用；如涉及侵权，提 issue 即可删除。

## 📄 许可证

[MIT](LICENSE)。健康信息（控糖、心理学临床词条等）仅为生活参考，不构成医疗建议，具体请遵医嘱。

## 更新日志

见 [CHANGELOG.md](CHANGELOG.md)。

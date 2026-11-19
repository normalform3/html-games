# HTML Games

一组可以直接在浏览器中运行的独立小游戏合集。每个游戏都有单独的目录和说明文档，**零构建、零后端依赖**，打开 `index.html` 即可游玩。

> 持续收录中。后续新增的小游戏会按同样的结构加入本仓库。
>
> GitHub 网页不会直接运行仓库里的 HTML；请克隆到本地打开，或启动一个静态服务器。

## 游戏列表

| 游戏 | 类型 | 玩法关键词 | 入口 |
| --- | --- | --- | --- |
| **铁壁王国** | 中世纪塔防 | 3 张地图 / 1–3 条路线 / 弓箭塔 / 法师塔 / 兵营士兵 / 10 波 Boss | [查看](games/ironhold-tower-defense/) |
| **元素沙盒** | 粒子物理沙盒 | 13 种材料 / 4 种自动装置 / 6 个关卡 / 3 张地图 / 实时合成音效 | [查看](games/element-sandbox/) |

## 本地运行

最简单的方式是直接用浏览器打开对应游戏的 `index.html`。

也可以在仓库根目录启动一个静态服务器：

```bash
git clone https://github.com/normalform3/html-games.git
cd html-games
python3 -m http.server 8000
```

然后访问：

```text
http://localhost:8000/games/ironhold-tower-defense/
```

## 目录结构

```text
html-games/
├── README.md
└── games/
    ├── element-sandbox/
    │   ├── index.html
    │   ├── README.md
    │   └── preview.png
    └── ironhold-tower-defense/
        ├── index.html
        ├── README.md
        ├── preview.png
        └── preview-levels.png
```

## 收录约定

新增游戏时，建议保持以下结构：

```text
games/<game-slug>/
├── index.html
├── README.md
└── preview.png
```

1. 在 `games/` 下建立新的游戏目录。
2. 游戏入口命名为 `index.html`，尽量单文件、无外部资源依赖。
3. 为游戏编写独立 `README.md`，至少包含玩法、操作、运行方式和预览图。
4. 更新本 README 的“游戏列表”表格。

## 技术说明

当前收录的游戏以原生 HTML / CSS / JavaScript 编写，使用 Canvas 2D 与 Web Audio API，不依赖框架或打包工具。桌面与移动端浏览器均可直接运行。

---

如果这个合集对你有帮助，欢迎 Star。

# 郭耀华教授课题组网站

郑州大学机械与动力工程学院 · 新能源与智能网联汽车研究团队（郭耀华教授课题组）官方网站。

- 线上地址：`https://java316.github.io/guoyh/`（GitHub 仓库 `java316/guoyh`，Pages 已开启）
- ⚠️ 待定：页内 5 处「郭教授个人主页」链接（`index.html` 第 141 / 159 / 860 / 895 / 907 行）与 `404.html` 第 55 行，目前都指向 `java316.github.io/guoyh/`——也就是**本站自己**，点击会在原页刷新。个人主页若另有地址，请把这 6 处一并改掉；若确认不再单独设个人主页，建议直接删掉这几个入口。

## 网站栏目（2026-09 面向学生与社会的活泼版）

| 栏目 | 内容 |
|------|------|
| 首页 Hero | 深蓝动态渐变 + 打字机标语（我们研究：……）+ 四项核心数据滚动动画 + 阅读进度条 |
| 最新动态 | Hero 下方三条滚动的"近期动态"卡片（学会获奖 / 欧洲行 / 领军人才项目），可直接跳转学术足迹 |
| 我们在做什么 | 4 个"真问题"场景卡（防侧翻/AEBS/能耗/轮胎盲区），面向公众与学生，通俗语言+关键数字 |
| 研究方向 | 三大方向彩色卡片 + 亮点清单；整体架构图收纳进折叠面板（减少框图堆砌） |
| 未来出行 | 前瞻板块"驶向未来"：智能轮胎即传感器、AI 进底盘回路、软件定义底盘、电动化迈向深水区 |
| 硬核成果 | 选项卡：获奖项目（对标图+院士评价+技术细节折叠）/ 科技奖励（历年奖励信息图）/ 重大项目 / 论文专著 / 知识产权 |
| 学术足迹 | 图文时间线（2025 学会获奖、米其林交流、Busworld 获奖、Rakheja 院士交流等），6 个条目各配一张现场照片 |
| 活动掠影 | 13 张照片瀑布流 + 点击灯箱放大（含左右切换与"n / 13"计数）；灯箱画廊只收录瀑布流内的照片 |
| 加入我们 | "为什么加入我们"4 张价值卡（真问题/真项目/真平台/真出路）+ 学生成绩 + 报考 FAQ 手风琴 + 招生横幅 |
| 课题组概况 / 联系方式 | 团队简介、依托平台、联系邮箱与地址 |

> 说明：本站内容不涉及企业单位与具体工程中心信息，以学科、团队与学术成果为主。
> 交互与体验：图片全站懒加载；导航栏提供「分享」按钮（移动端调用系统分享、桌面端一键复制链接）；分享缩略图与站点图标齐备。

## 文件结构

```
guoyh/                                  # 仓库根目录 = 本文件夹内容
├── index.html          # 网站首页（单页，纯静态，改内容无需构建）
├── 404.html            # 自定义 404 页面（GitHub Pages 自动使用）
├── robots.txt          # 搜索引擎抓取指引
├── sitemap.xml         # 站点地图（提交给搜索引擎）
├── README.md
└── images/                           # 全站图片与格式文件 39 个，统一平铺存放（无子目录）
    ├── site.css                      # 全站样式表 = Tailwind 预编译产物 + Font Awesome Solid 子集（29 KB）
    ├── fa-solid-900-subset.woff2     # 图标字体子集，仅含本站实际用到的 45 个图标（5.8 KB）
    ├── og-cover.jpg                  # 分享缩略图（微信/微博等转发卡片，1200×630）
    ├── favicon.png                   # 站点图标
    ├── apple-touch-icon.png          # iOS 主屏图标
    ├── fig1_research_directions.webp # 团队三大研究方向架构图（已去除相关单位字样）
    ├── fig3_tech_transfer.webp       # 机-电-控协同技术迁移路径（已去除相关单位字样）
    ├── fig5_projects.webp            # 代表性科研项目信息图
    ├── fig6_awards.webp              # 主要科技奖励信息图
    ├── fig7_papers.webp              # 代表性论文与专著信息图
    ├── fig8_innovations.webp         # 获奖项目 · 四大技术创新总览
    ├── fig9_benchmark.webp           # 获奖项目 · 关键指标国际对标
    ├── fig10_ip.webp                 # 获奖项目 · 核心知识产权与标准
    ├── sae_*.webp                    # 获奖项目技术图 6 张（整理自中国汽车工程学会答辩PPT，品牌中性化）
    └── photo*.webp                   # 20 张现场照片：13 张用于活动掠影瀑布流、6 张用于学术足迹时间线、1 张为招生横幅背景（不含个人头像）
```

> 图片：34 张内容图已统一转为 WebP（照片 q82 有损、文本型信息图无损），`images/` 总体积由约 4.4 MB 降至 2.99 MB；`og-cover.jpg` 与两个图标**刻意保留 JPEG/PNG**，因为微信、微博、Telegram 等社交平台爬虫对 WebP 的 og:image 支持不稳定，图标格式也有平台硬性要求。所有 `<img>` 均带 `width`/`height`，浏览器可提前预留版面、避免加载时页面跳动（CLS）。
>
> 样式：全站样式已**完全本地化**，由 `images/site.css` 一个文件提供（Tailwind 预编译产物 + Font Awesome Solid 子集），加上 `index.html` 内的 `<style>` 自定义动效。站点**不再引用任何第三方 CDN**，也没有 `.js` 外部文件；`images/` 因此同时存放图片与格式文件（css / woff2）。原先的 `assets/award/`、`assets/photos/` 子目录已取消，全部平铺在 `images/` 根下。

## 加载性能（2026-09 本地化改造）

改造前主页依赖 3 个境外 CDN，且**全部是阻塞渲染资源**，在国内网络下实测：

| 资源 | 体积 | 冷加载实测 |
|------|------|-----------|
| `cdn.tailwindcss.com`（Tailwind 运行时） | 407 KB | **12.17 s**（含 302 跳转） |
| `cdnjs.cloudflare.com`（Font Awesome all.min.css） | 102 KB | **连接超时 30 s** |
| `fonts.googleapis.com`（Noto Serif/Sans SC） | 879 KB CSS | 含 808 条 @font-face、202 个 woff2 分片、8 种字重 |

改造后：第三方阻塞请求 **3 → 0**，样式与图标改为 1 个本地 CSS（29 KB，gzip 6.3 KB）+ 1 个子集字体（5.8 KB，并已 `preload`）。Google Fonts 原本请求了 8 种字重，而页面只用到 4 种（且 sans 缺 600/900、serif 缺 500），现已改用**系统原生中文字体栈**（苹方 / 鸿蒙黑 / 微软雅黑 / 思源，衬线用 Georgia + 宋体系），零字体下载。FontAwesome 原本加载全量 ~2000 图标，现只保留本站用到的 45 个，字体从 150 KB 子集化到 5.8 KB（3.9%）。

> 字体说明：改用系统字体栈是**性能优先**的取舍，各平台自动使用中文字体，视觉与原先的 Noto 略有差异。若希望恢复 Noto 的观感，可改为自托管思源黑体/宋体的子集（需新增约 1–3 MB 字体文件），不建议再引回 Google Fonts CDN。

### 改造前后实测对比

同一环境实测（本机 `python -m http.server` + 浏览器，热缓存；数字仅用于同环境前后横向对比，线上 GitHub Pages 会受访问者网络影响）：

| 指标 | 改造前 | 改造后 |
|------|--------|--------|
| 首次内容绘制 FCP | 732 ms | **120 ms** |
| DOMContentLoaded | — | **41 ms** |
| load 事件 | 985 ms | **56 ms** |
| 阻塞渲染的第三方资源 | 3 个（境外 CDN） | **0 个** |
| 阻塞渲染资源总数 | 3 个 | **1 个**（本地 `site.css` 28.5 KB） |
| 首屏关键路径下载量 | 约 1.39 MB（均为境外阻塞资源） | **约 144 KB**（全部本地） |
| 字体下载量 | Google Fonts 202 个 woff2 分片 + FA 全量 150 KB | **5.8 KB**（仅 FA 子集，中文走系统字体） |
| `images/` 总体积 | 约 4.31 MB（37 张 JPEG/PNG） | **2.99 MB**（34 张 WebP + 3 个刻意保留） |
| 缺少 `width`/`height` 的 `<img>` | 35 个（加载时页面跳动 CLS） | **0 个** |
| 控制台输出 | 1 条警告（Tailwind CDN 不宜用于生产） | **0 error / 0 warning** |

冷加载（首次访问、无缓存）差距更显著：改造前 `cdn.tailwindcss.com` 单个资源就要 **12.17 s**、`cdnjs.cloudflare.com` 在国内网络下**连接超时 30 s**，页面在此期间白屏；改造后已无任何境外请求，白屏时间只取决于本地/ Pages 的 144 KB 传输。

### 功能回归校验结果

改造后已用浏览器逐项回归，全部通过：

- **图片**：34 张内容图经真实滚动与选项卡交互全部加载成功，0 失败、0 HTTP 错误；
- **图标**：45 个图标码点与子集字体 cmap 完全一致（零缺失、零冗余），67 个图标元素全部有字形；
- **交互**：5 个选项卡切换正常；灯箱打开/上一张/下一张/首尾环绕/关闭与「n / 13」计数正常；6 个折叠面板可开合；移动端汉堡菜单展开收起正常（8 个链接）；分享按钮、回到顶部、阅读进度条、打字机标语、数字滚动（106 / 25 / 7 / 30）、滚动显现动画均正常；
- **地址**：页脚与正文均显示「郑州大学科学大道校区」，旧的错误写法已全站清除、零残留。

> 说明：活动掠影瀑布流实为 13 张照片，灯箱计数因此是「n / 13」；另外 7 张照片分别用于学术足迹时间线（6 张）与招生横幅背景（1 张），不属于灯箱画廊。


## GitHub Pages 部署步骤（仓库 `java316/guoyh`）

> ### 🚨 必读：不要用网页端拖拽 `images` 文件夹
>
> 2026-09-13 实测发现，仓库里 **`images/` 目录整个不存在**：39 个文件中有 15 个被**平铺丢到了仓库根目录**，另外 24 个**根本没上传成功**。而 `index.html` 引用的是 `images/xxx`，于是**全站图片、`site.css` 样式表、图标字体全部 404**——这就是「图片全部无法显示」的直接原因。
>
> GitHub 网页端的 `Upload files` **不支持拖入文件夹**：拖进去时文件夹会被拆开、只传里面的文件，且数量多时会静默丢弃一部分。务必用下面的方式之一。

### 方式 A：运行部署脚本（最推荐，一次到位）

桌面上已备好 `部署课题组网站到GitHub.sh`，它会**克隆线上仓库 → 清除根目录散落文件 → 按正确层级写入 `images/` 全部 39 个文件 → 提交推送**，保留提交历史、不使用 force push，执行前会列出改动清单并要求输入 `yes` 确认。

在 Git Bash 中执行：

```bash
bash "/c/Users/Lenovo/Desktop/部署课题组网站到GitHub.sh"
```

推送时 Git Credential Manager 会弹窗，用 GitHub 账号登录一次即可（凭据由 Windows 记住，之后不再询问）。

### 方式 A2：手工命令行（不想用脚本时）

```bash
cd /c/Users/Lenovo/Desktop/ktz
git init
git add .
git commit -m "课题组网站：性能优化版 + 修正 images 目录层级"
git branch -M main
git remote add origin https://github.com/java316/guoyh.git
git pull --rebase origin main        # 合并仓库现有内容，首次会提示输入凭据
git push origin main
```

- 走这条路时，根目录那 15 个误传的散落文件（`photo29.webp`、`site.css`、`og-cover.jpg` 等）**不会被自动清掉**，需另行删除：仓库页逐个点进去 → 右上角垃圾桶图标 → `Commit changes`；或 `git rm` 后重新 push。脚本方式已包含这一步。

### 方式 B：网页端（必须先建目录）

1. 仓库页 → `Add file` → `Create new file`；
2. 文件名输入 `images/.keep`（**输入斜杠时 GitHub 会自动创建 `images` 目录**）→ `Commit changes`；
3. 进入刚建好的 `images/` 目录 → `Add file` → `Upload files`；
4. **打开文件资源管理器进入 `images` 文件夹内部**，全选 39 个文件（不是选文件夹本身）拖入上传区；
5. 确认上传列表显示 **39 个文件**后再 `Commit changes`——数量不对就是又被丢弃了，需重传；
6. 根目录的 5 个文件（`index.html`、`404.html`、`robots.txt`、`sitemap.xml`、`README.md`）单独上传覆盖；
7. 删除根目录里那 15 个误传的散落文件。

### 上传后自检（必做）

浏览器直接访问下面 4 个地址，**全部返回图片/文本而不是 404** 才算成功：

```
https://java316.github.io/guoyh/images/site.css
https://java316.github.io/guoyh/images/photo29.webp
https://java316.github.io/guoyh/images/og-cover.jpg
https://java316.github.io/guoyh/images/fa-solid-900-subset.woff2
```

再打开首页 `https://java316.github.io/guoyh/`，按 F12 → `Network` 面板刷新，确认**没有红色 404 条目**；`Console` 面板无报错。

### 其他

- Pages 开启位置：仓库 → `Settings` → `Pages` → `Deploy from a branch` → Branch 选 `main` / `(root)` → `Save`（当前已开启）。
- 可选：把 `https://java316.github.io/guoyh/sitemap.xml` 提交到百度/Google 站长平台，加快收录。

## 绝对地址与外部链接

`index.html` 的 `rel="canonical"`、`og:url`、`og:image`、`twitter:image` 与 JSON-LD 共 6 处，以及 `sitemap.xml`、`robots.txt`、`404.html`（3 处 `/guoyh/` 根绝对路径）都已统一指向正式地址 `https://java316.github.io/guoyh/`。

> `404.html` 必须用 `/guoyh/...` 这种**根绝对路径**，不能用相对路径——GitHub Pages 会在任意深度的错误路径上渲染它，相对路径会解析错。
> 若日后换成自定义域名或改仓库名，上述所有绝对地址都要同步改，否则社交分享卡片会裂图。

### 外部链接现状（2026-09-13 实测）

| 链接 | 用途 | 状态 |
|------|------|------|
| `https://java316.github.io/guoyh/` | 本站正式地址 | HTTP 200 |
| `https://www5.zzu.edu.cn/mech/` | 机械与动力工程学院官网（页脚相关链接） | HTTP 200 |

> 已修正 1：学院官网原写作 `https://www5.zzu.edu.cn/cmee/`，实测 404，已更正为官方地址 `https://www5.zzu.edu.cn/mech/`（页面标题「郑州大学机械与动力工程学院」）。
> 已修正 2：`sitemap.xml` 原有两条 `<loc>`（`guoyh-group/` 与 `guoyh/`），统一到 `guoyh` 后会变成重复条目，已合并为一条。
> 待你决定：页内 6 处「个人主页」入口目前指向本站自身，见文首 ⚠️ 说明。



## 关于「个人主页」（已失效的旧说明，勿照做）

早前的计划是：课题组网站放 `guoyh-group` 仓库，郭教授个人主页放 `guoyh` 仓库，两者互相链接；本文件夹里曾有一个 `主页更新版-index.html`，用途是覆盖上传到 `guoyh` 仓库、给个人主页加上「课题组网站」入口。

**现在的实际情况已经变了，旧步骤不能再执行：**

- `guoyh-group` 仓库目前返回 GitHub `Site not found`（404），已不可用；
- 课题组网站**已经部署在 `guoyh` 仓库**，`https://java316.github.io/guoyh/` 打开的就是本站；
- `主页更新版-index.html` 这个文件已不在本文件夹内。

> ⛔ **千万不要**再把任何「个人主页」版本的 `index.html` 上传覆盖 `guoyh` 仓库——那会直接把课题组网站替换掉。

**遗留待办（需要你决定）**：站内 6 处「郭教授个人主页 / 教授个人主页」入口（`index.html` 第 141 / 159 / 860 / 895 / 907 行、`404.html` 第 55 行）现在都指向本站自己，点击等于原地刷新。三种处理方式任选：

1. 个人主页另建仓库（例如 `guoyh-home`）或改用学校师资主页，把这 6 处换成新地址；
2. 确认不再单独设个人主页，直接删掉这 6 个入口（`404.html` 里两个按钮会变成重复，删掉 ghost 那个）；
3. 暂时保留不动——链接能打开（HTTP 200），只是语义上重复。

## 内容维护


- 网站为纯静态单页，**改内容无需构建**：编辑 `index.html` 的文字、图片或结构后直接上传即可更新。
- ⚠️ 一个例外：Tailwind 已改为**预编译**（`images/site.css`），只包含当前 HTML 里出现过的工具类。如果你在页面里新增了此前从未用过的 Tailwind 类名（例如第一次用 `text-rose-500`），它不会自动生效，需要重新编译一次：
  ```bash
  npm install -D tailwindcss@3.4.17
  npx tailwindcss -c tailwind.config.js -i input.css -o images/site.css --minify
  ```
  （`tailwind.config.js` 的 `content` 指向 `index.html`，主题色 `primary:#1e3a5f` / `secondary:#c9a227` 与字体栈需与页面保持一致。）
- 更新建议：
  - 新动态：编辑 `#news` 板块的三张卡片（标题 / 日期 / 一句话说明）；
  - 新获奖、新论文：在"硬核成果"对应选项卡中按时间倒序插入条目；新增获奖需重新生成并导出 `fig6_awards.webp`；
  - 新活动：在"学术足迹"时间线追加条目，把照片转成 WebP 后放入 `images/`，再加入"活动掠影"瀑布流（建议长边不超过 1600px、照片 q82、文本型信息图用无损）。转换示例：
    ```bash
    python -c "from PIL import Image;Image.open('photo30.jpeg').convert('RGB').save('images/photo30.webp','WEBP',quality=82,method=6)"
    ```
    记得给新 `<img>` 补上真实的 `width` / `height`，与站内其余图片保持一致，避免加载跳动。
- 新增图标：`site.css` 里的 Font Awesome 只子集化了当前用到的 45 个图标。若要用新图标，需把对应字形加回子集并重新生成 `fa-solid-900-subset.woff2`，否则该图标会显示为空白。
- 注：本节原先提到的 `gen_figures.py`（架构图生成脚本）并不在本文件夹内，信息图目前是按上述方式单独导出为 WebP 的。


## 数据来源

内容凝练自课题组申报材料（个人介绍精简版 20260905、科学研究素材 20260904、社会服务素材 20260903 等）、中国汽车工程学会科技进步奖答辩PPT（附件1，2025 年 9 月）及个人主页既有公开内容。获奖项目素材已做品牌中性化处理：不出现企业单位名称，不呈现整车销量与销售额等企业业绩数据；专利证书原件因含专利权人信息未直接上墙，改以专利号+名称的信息图呈现。涉密项目仅列名称，未公开经费明细。

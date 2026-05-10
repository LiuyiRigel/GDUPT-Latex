# 🎓 广东石油化工学院（GDUPT）本科毕业论文 / 设计 LaTeX 模板

<div align="center">

[![LaTeX](https://img.shields.io/badge/LaTeX-XeLaTeX-008080?style=for-the-badge&logo=latex&logoColor=white)](https://github.com/LiuyiRigel/GDUPT-Latex)
[![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20Linux%20%7C%20macOS-blue?style=for-the-badge)](https://github.com/LiuyiRigel/GDUPT-Latex)
[![BibTeX](https://img.shields.io/badge/BibTeX-GB%2FT%207714--2015-orange?style=for-the-badge)](https://github.com/LiuyiRigel/GDUPT-Latex)
[![License](https://img.shields.io/github/license/LiuyiRigel/GDUPT-Latex?style=for-the-badge)](./LICENSE)
[![Stars](https://img.shields.io/github/stars/LiuyiRigel/GDUPT-Latex?style=for-the-badge)](https://github.com/LiuyiRigel/GDUPT-Latex/stargazers)

**现代化中文排版 · 模块化结构 · XeLaTeX 驱动 · 本地 & Overleaf 双支持**

*让 GDUPT 学子告别 Word 排版地狱 🕊️*

</div>

---

## 📑 目录

- [✨ 功能亮点](#-功能亮点)
- [👥 适用人群](#-适用人群)
- [📦 项目结构](#-项目结构)
- [🚀 快速开始](#-快速开始)
- [📚 参考文献](#-参考文献)
- [🖼️ 图表支持](#️-图表支持)
- [⚙️ 自定义配置](#️-自定义配置)
- [💡 编译建议](#-编译建议)
- [❗ 常见问题](#-常见问题)
- [🙏 致谢](#-致谢)

---

## ✨ 功能亮点

| 功能 | 说明 |
|------|------|
| 🎓 **格式合规** | 严格遵循 GDUPT 本科毕业论文（设计）格式要求 |
| 🇨🇳 **中文排版** | 基于 `XeLaTeX` + `ctex`，完美支持中英混排 |
| 🧩 **模块化** | 章节独立文件，团队协作 & 大型论文轻松管理 |
| 📚 **参考文献** | `BibTeX` + `gbt7714`（GB/T 7714-2015 标准）开箱即用 |
| 📄 **完整前导页** | 诚信承诺书、中英文摘要、目录、图表索引 |
| 📎 **附录支持** | 外文调研报告、书面翻译、附录章节 |
| 🏛️ **评阅表格** | 内置答辩委员会、评阅书、简历、符号说明模板 |
| 🖼️ **图表增强** | `booktabs` 三线表、`longtable` 长表格、`subcaption` 子图 |
| 🛠️ **多平台** | VS Code / Overleaf / TeXstudio 均可编译 |
| 📖 **新手友好** | 只需修改 `Info.tex` 和 `parts/` 即可开始写作 |

---

## 👥 适用人群

- 🎓 广东石油化工学院 **本科毕业生**（毕业论文 / 毕业设计）
- 📝 需要符合 **GDUPT 格式规范** 的学术写作者
- 🔰 无 LaTeX 基础但希望 **专注内容、摆脱排版焦虑** 的同学
- 👨‍🏫 指导老师批量审阅 **格式统一** 的学生论文

---

## 📦 项目结构

```text
GDUPT-Latex/
├── thesis.tex                              # 🔧 主文档（在此编译）
├── Info.tex                                # ✏️ 论文元信息（学号、姓名、题目等）
├── gduptbe.cls                             # ⚙️ 模板类文件（格式定义）
├── thesis.pdf                              # 📄 预编译示例 PDF
│
├── bib/
│   ├── refs.bib                            # 📚 参考文献数据库
│   └── thuthesis-*.bbx/cbx/bst            # 参考文献样式文件
│
├── parts/                                  # 📝 正文各章节
│   ├── abstract.tex                        #   中英文摘要
│   ├── chap01.tex  ~  chap04.tex           #   第 1~4 章
│   ├── acknowledgements.tex                #   致谢
│   ├── appendix.tex                        #   附录
│   ├── appendix-survey.tex                 #   外文调研报告
│   ├── appendix-translation.tex            #   外文书面翻译
│   ├── committee.tex                       #   答辩委员会
│   ├── resolution.tex                      #   评阅书
│   ├── resume.tex                          #   简历
│   └── denotation.tex                      #   符号说明
│
├── imgs/                                   # 🖼️ 图片资源（校徽、Logo 等）
├── figs/                                   # 📊 插图 & 扫描件
└── 广东石油化工学院2026届毕业论文（设计）表格/  # 📋 官方表格附件
```

---

## 🚀 快速开始

### 1️⃣ 安装环境

| 工具 | 用途 | 下载 |
|------|------|------|
| **TeX Live** | LaTeX 发行版（必须） | [tug.org/texlive](https://tug.org/texlive/) |
| **VS Code** | 推荐编辑器 | [code.visualstudio.com](https://code.visualstudio.com/) |
| **LaTeX Workshop** | VS Code 插件 | 扩展商店搜索安装 |

> 💡 不想本地安装？直接上传至 [Overleaf](https://www.overleaf.com/) 使用 XeLaTeX 编译即可。

### 2️⃣ 填写论文信息

打开 `Info.tex`，修改以下内容：

```latex
\stunum{202102180102}           % 学号
\author{张~三}                  % 姓名
\advisor{张~翼~成(讲师)}        % 导师
\school{自动化}                 % 学院
\dept{电气工程及其自动化}       % 专业
\title{...}                     % 中文题目
\entitle{...}                   % 英文题目
\designtime{...}                % 设计起止时间
```

### 3️⃣ 编写正文

在 `parts/` 目录下编辑各章节：

| 文件 | 内容 |
|------|------|
| `abstract.tex` | 中英文摘要 & 关键词 |
| `chap01.tex` | 第一章（引言/背景） |
| `chap02.tex` | 第二章 |
| `chap03.tex` | 第三章 |
| `chap04.tex` | 第四章（总结与展望） |
| `acknowledgements.tex` | 致谢 |
| `appendix.tex` | 附录内容 |

### 4️⃣ 管理参考文献

编辑 `bib/refs.bib`，按 BibTeX 格式添加引用：

```bibtex
@article{zhang2025,
  title  = {深度学习在故障诊断中的应用},
  author = {张三 and 李四},
  journal= {自动化学报},
  year   = {2025},
  volume = {51},
  pages  = {1--15}
}
```

在正文中用 `\cite{zhang2025}` 引用。

### 5️⃣ 编译论文

**VS Code（推荐）：** 打开 `thesis.tex` → 按 `Ctrl + Alt + B` → 选择 `Recipe: latexmk (xelatex)`

**命令行：**
```bash
xelatex thesis.tex
bibtex thesis
xelatex thesis.tex
xelatex thesis.tex
```

> ⚠️ 必须编译 **2~3 次** 以确保交叉引用、目录和参考文献正确生成。

---

## 📚 参考文献

默认使用 **GB/T 7714-2015** 国家标准（顺序编码制）。

模板内置了 `thuthesis` 系列的 `.bst` / `.bbx` / `.cbx` 样式文件，支持：
- `numeric`（顺序编码制）
- `author-year`（著者-出版年制）

如需切换样式，修改 `thesis.tex` 中的 `\bibliographystyle` 即可。

---

## 🖼️ 图表支持

模板已预加载以下宏包，无需额外配置：

| 宏包 | 用途 | 示例命令 |
|------|------|----------|
| `graphicx` | 图片插入 | `\includegraphics{...}` |
| `subcaption` | 子图排版 | `\subcaptionbox{...}` |
| `booktabs` | 三线表 | `\toprule, \midrule, \bottomrule` |
| `longtable` | 跨页长表格 | `\begin{longtable}...` |
| `multirow` | 单元格合并 | `\multirow{2}{*}{...}` |
| `siunitx` | SI 单位对齐 | `\SI{10}{\meter}` |

---

## ⚙️ 自定义配置

### 修改中文字体

在 `gduptbe.cls` 或 `Info.tex` 中调整：

```latex
\setCJKmainfont{SimSun}     % 宋体（正文）
\setCJKsansfont{SimHei}     % 黑体（标题）
\setCJKmonofont{STKaiti}    % 楷体
```

### 调整页面边距

在 `Info.tex` 中修改 `geometry` 参数：

```latex
\usepackage[top=2.8cm, bottom=2.2cm, outer=2.2cm, inner=2.8cm]{geometry}
```

### 隐藏/显示图表索引

在 `thesis.tex` 中取消注释：

```latex
\listoffigures   % 插图索引
\listoftables    % 表格索引
```

---

## 💡 编译建议

| 项目 | 推荐 | 备注 |
|------|------|------|
| 编译器 | **XeLaTeX** | 中文字体支持最佳 |
| 文献工具 | **BibTeX** | 传统稳定方案 |
| 编辑器 | **VS Code** + LaTeX Workshop | 实时预览、自动补全 |
| 在线编译 | **Overleaf** | 无需安装，选 XeLaTeX 编译器 |
| 大论文 | **本地编译** | 编译速度更快 |

---

## ❗ 常见问题

<details>
<summary><b>❌ XeLaTeX is required</b></summary>

当前编译器不是 XeLaTeX，请在 VS Code 或 Overleaf 中切换编译链为 `XeLaTeX`。
</details>

<details>
<summary><b>❌ 中文显示为乱码</b></summary>

缺少中文字体。Windows 用户确保安装了 **宋体（SimSun）/ 黑体（SimHei）/ 楷体（KaiTi）**；macOS/Linux 用户可安装中文字体包或修改 `gduptbe.cls` 中的字体设置。
</details>

<details>
<summary><b>❌ 图片无法显示</b></summary>

检查：① 图片路径是否正确 ② 文件后缀是否匹配（`.pdf` / `.png` / `.jpg`）③ 图片是否放在 `imgs/` 或 `figs/` 目录下。
</details>

<details>
<summary><b>❌ 参考文献引用显示 [?]</b></summary>

需要完整编译链：`XeLaTeX → BibTeX → XeLaTeX → XeLaTeX`，共 4 步。确保 `bib/refs.bib` 中存在对应条目。
</details>

<details>
<summary><b>❌ Overleaf 编译超时</b></summary>

Overleaf 免费版有编译时间限制。建议大论文在本地编译，或精简图片大小。
</details>

---

## 🙏 致谢

本模板的诞生离不开以下开源项目的启发与代码贡献：

| 项目 | 贡献 |
|------|------|
| [thuthesis](https://github.com/tuna/thuthesis) | 参考文献样式、类文件架构 |
| [phd-thesis-template](https://github.com/kks32/phd-thesis-template) | 模块化章节结构设计 |
| [LZUthesis](https://github.com/szsdk/LZUthesis) | 中文排版与格式参考 |
| [CTeX](http://www.ctex.org/) | 中文 LaTeX 生态核心支持 |

**特别感谢：** 张翼成老师（`zhangyicheng@gdupt.edu.cn`）创建并维护此模板。

---

<div align="center">

### ⭐ 如果这个模板帮到了你，请给个 Star！

[![Stars](https://img.shields.io/github/stars/LiuyiRigel/GDUPT-Latex?style=for-the-badge)](https://github.com/LiuyiRigel/GDUPT-Latex/stargazers)

让更多 GDUPT 学子摆脱 Word 排版地狱 🕊️


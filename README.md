# 广东石油化工学院（GDUPT）本科毕业论文 / 设计 LaTeX 模板

<div align="center">

![LaTeX](https://img.shields.io/badge/LaTeX-XeLaTeX-008080?style=for-the-badge\&logo=latex\&logoColor=white)

![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20Linux%20%7C%20macOS-blue?style=for-the-badge)

![BibTeX](https://img.shields.io/badge/BibTeX-GB%2FT%207714--2015-orange?style=for-the-badge)

![Documentation](https://img.shields.io/badge/docs-ready-brightgreen?style=for-the-badge)

[![License](https://img.shields.io/github/license/Ileriayo/markdown-badges?style=for-the-badge)](./LICENSE)

现代化中文排版 · 模块化结构 · XeLaTeX 驱动 · 本地编译友好

[![GitHub Stars](https://img.shields.io/github/stars/LiuyiRigel/GDUPT-Latex?style=for-the-badge)](https://github.com/LiuyiRigel/GDUPT-Latex/stargazers)


</div>

---

## ✨ Features

- 🎓 适配 GDUPT 本科毕业论文格式
- ⚡ 基于 `XeLaTeX` 的现代中文排版
- 🧩 模块化章节结构，适合大型论文
- 📚 支持 `BibTeX + gbt7714`
- 🖼️ 内置图表、长表格、子图支持
- 🛠️ VS Code / Overleaf / TeXstudio 开箱即用
- 📖 适合无 LaTeX 基础用户快速上手

---

## 📦 项目结构

```text
.
├── thesis.tex                # 主文档
├── Info.tex                  # 论文信息
├── gduptbe.cls               # 模板类文件
├── bib/
│   └── refs.bib              # 参考文献数据库
├── parts/
│   ├── abstract.tex
│   ├── chap01.tex ~ chap04.tex
│   ├── acknowledgements.tex
│   ├── appendix.tex
│   └── ...
├── imgs/                     # 图片资源
└── figs/

```

---

## 🚀 Quick Start

### 1. 安装环境

推荐环境：

- `TeX Live`
- `VS Code`
- `LaTeX Workshop`


---

### 2. 打开项目

打开：

```text
thesis.tex
```

VS Code 编译快捷键：

```text
Ctrl + Alt + B
```

若出现：

```text
Recipe: latexmk (xelatex)
```

则环境配置成功。

---

### 3. 编辑论文信息

修改：

```text
Info.tex
```

填写：

- 学号 / 姓名
- 导师 / 学院 / 专业
- 论文题目
- 学校名称
- 设计时间

---

### 4. 编写正文

正文位于：

```text
parts/
```

主要文件：

```text
abstract.tex
chap01.tex
chap02.tex
chap03.tex
chap04.tex
acknowledgements.tex
```

---

### 5. 添加参考文献

编辑：

```text
bib/refs.bib
```

BibTeX 示例：

```bibtex
@article{example,
  title={Example Title},
  author={Author},
  journal={Journal},
  year={2025}
}
```

---

### 6. 编译论文

推荐编译顺序：

```bash
xelatex thesis.tex
bibtex thesis
xelatex thesis.tex
xelatex thesis.tex
```

---

## 📚 参考文献

默认采用：

```text
GB/T 7714-2015
```

通过：

```latex
\bibliography{bib/refs}
```

自动加载参考文献数据库。

---

## 🖼️ 图表支持

| 功能 | 宏包 |
|---|---|
| 图片插入 | `graphicx` |
| 子图 | `subcaption` |
| 专业表格 | `booktabs` |
| 长表格 | `longtable` |
| 多行合并 | `multirow` |
| SI 单位对齐 | `siunitx` |

---

## ⚙️ 自定义配置

### 修改字体

```latex
\setCJKmainfont{SimSun}
```

可在：

```text
gduptbe.cls / Info.tex
```

中修改。

### 修改参考文献样式

当前默认：

```text
gbt7714
```

如需更换，可修改 `.bst` 或切换 `biblatex`。

---

## 💡 编译建议

| 项目 | 推荐 |
|---|---|
| 编译器 | `XeLaTeX` |
| 文献工具 | `BibTeX` |
| 编辑器 | VS Code |
| 插件 | LaTeX Workshop |
| 大论文 | 本地编译 |

---

## ❗ 常见问题

### XeLaTeX is required

当前编译器不是：

```text
XeLaTeX
```

请切换编译链。

### 中文乱码

请安装字体：

```text
SimSun / STSong / STKaiti
```

### 图片无法显示

检查：

- 图片路径
- 文件后缀
- `imgs/` / `figs/` 目录

---

## 🌐 推荐工作流

```text
VS Code → LaTeX Workshop → latexmk → XeLaTeX → BibTeX → PDF
```

---

## 🙏 Acknowledgements

参考与借鉴：

- `thuthesis`
- `phd-thesis-template`
- GDUPT 本科论文规范
- 开源 LaTeX 社区生态

---

<div align="center">

### ⭐ Star this repository if it helps you

让更多 GDUPT 学生摆脱 Word 地狱。


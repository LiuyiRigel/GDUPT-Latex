
# GDUPT 本科毕业论文 LaTeX 模板指北

[![Licence](https://img.shields.io/github/license/Ileriayo/markdown-badges?style=for-the-badge)](./LICENSE)
![LaTeX](https://img.shields.io/badge/latex-%23008080.svg?style=for-the-badge&logo=latex&logoColor=white)  

![Documentation](https://img.shields.io/badge/documentation-yes-brightgreen)  

参考文献遵循GB/T 7741-2015标准

本仓库提供广东石油化工学院（GDUPT）本科毕业论文/设计模板，基于 `gduptbe` 自定义类开发。当前模板适用于 `XeLaTeX` 编译环境，可快速生成符合校内毕业论文格式的 PDF 文档。

## 主要内容
- `thesis.tex`：论文主文档，负责加载信息、生成封面、目录、正文、致谢和参考文献。
- `Info.tex`：论文元数据配置文件，包含作者、导师、院系、题目、日期等信息。
- `gduptbe.cls`：模板类文件，定义版面、标题、章节、目录、参考文献样式等全局格式。
- `bib/refs.bib`：参考文献 BibTeX 数据库。
- `parts/`：论文正文模块，包括摘要、章节、附录、致谢等可拆分文件。
- `imgs/`：论文插图资源目录。
- `GDUPT学报/`：学报模板与规范资料。
- `广东石油化工学院2026届毕业论文（设计）表格/`：学校表格及表单样例。

## 适用范围
- GDUPT 本科毕业论文/设计项目
- 适合希望用 LaTeX 编写毕业论文的本科生
- 支持封面、摘要、目录、正文、结论、参考文献、致谢、附录等常规章节结构

---

## 快速开始

### 快速安装（VS Code + TeX Live，本地编译）
1. 安装 TeX Live：
   - 下载并安装 TeX Live（Windows 版），建议使用默认安装选项。
   - 如果下载较慢，可使用国内镜像或直接安装 `TeX Live` 的最小安装后再补充宏包。
2. 安装 VS Code：
   - 下载并安装 Visual Studio Code。
3. 安装 LaTeX 插件：
   - 打开 VS Code，进入扩展商店，安装 `LaTeX Workshop`。
4. 检查配置：
   - VS Code 中打开 `thesis.tex`，按 `Ctrl+Shift+P`，运行 `LaTeX Workshop: Build with recipe`。
   - 如果提示 `xelatex`，说明已成功识别 TeX Live。
5. 运行编译：
   - 在 VS Code 中按 `Ctrl+Alt+B`（或点击左侧 LaTeX 图标），使用默认构建命令。

### 项目使用步骤
1. 下载本仓库代码到本地。
2. 使用支持 `XeLaTeX` 的编辑器打开 `thesis.tex`。
3. 编辑 `Info.tex`，填写：
   - 学号、姓名、导师、学院、专业、班级、论文题目
   - 学校名称、设计时间、封面图片等
4. 编辑 `parts/` 目录中的章节文件：
   - `parts/abstract.tex`
   - `parts/chap01.tex`、`parts/chap02.tex`、`parts/chap03.tex`、`parts/chap04.tex`
   - `parts/acknowledgements.tex`
5. 在 `bib/refs.bib` 中添加 BibTeX 文献项。
6. 编译命令：
   - `XeLaTeX thesis.tex`
   - `BibTeX thesis`
   - `XeLaTeX thesis.tex`
   - `XeLaTeX thesis.tex`

> 推荐在 Overleaf、TeXstudio、VS Code + LaTeX Workshop 等环境下使用 `XeLaTeX`。如果出现字体或中文问题，请确认系统已安装所需中文字体。

---

## 文件目录结构

```text
.
├── .gitignore
├── .vscode/
├── README.md
├── gduptbe.cls
├── Info.tex
├── thesis.tex
├── thesis.pdf
├── bib/
│   └── refs.bib
├── figs/
├── imgs/
├── parts/
│   ├── abstract.tex
│   ├── chap01.tex
│   ├── chap02.tex
│   ├── chap03.tex
│   ├── chap04.tex
│   ├── acknowledgements.tex
│   ├── appendix.tex
│   ├── appendix-survey.tex
│   ├── appendix-translation.tex
│   └── ...
├── GDUPT学报/
│   └── 学报的论文模板-2024-04.docx
└── 广东石油化工学院2026届毕业论文（设计）表格/
    ├── 1.毕业论文成绩评分依据及评定标准.docx
    ├── 9.毕业论文（设计）封面.doc
    └── ...
```

> 其中 `thesis.pdf` 为示例输出文件，编译过程中会自动生成 `thesis.aux`、`thesis.log`、`thesis.out`、`thesis.synctex.gz` 等辅助文件。

---

## 常用功能说明

### 1. 论文结构拆分
模板采用 `\include{parts/xxx}` 方式管理正文模块。
- `parts/abstract.tex`：中英文摘要与关键词
- `parts/chap01.tex` ~ `parts/chap04.tex`：正文章节
- `parts/acknowledgements.tex`：致谢
- `parts/appendix.tex`：附录

### 2. 论文元信息定义
`Info.tex` 中定义：
- `\title{}` / `\entitle{}`：中英文题目
- `\author{}` / `\advisor{}`：作者与指导老师
- `\school{}` / `\dept{}`：学院与专业
- `\stucls{}`：班级
- `\designtime{}`：设计时间
- `\university{}`：学校名称

### 3. 参考文献支持
模板使用 `gbt7714` 风格，同时在 `thesis.tex` 内以 `\bibliography{bib/refs}` 引入文献数据库。

### 4. 图片与表格支持
模板类与 `Info.tex` 已预配置常用宏包：
- `graphicx`：插图支持
- `subcaption`：子图支持
- `booktabs`、`multirow`、`longtable`、`threeparttable`：专业表格排版
- `siunitx`：国际单位制和数字对齐

### 5. 章节与目录样式
`gduptbe.cls` 已设置：
- 中英文封面样式
- 目录标题格式 `目 录`
- 参考文献标题 `参考文献`
- `\frontmatter` / `\mainmatter` / `\backmatter` 分段

### 6. 附件与声明
模板包含：
- `\statement`：毕业论文诚信声明
- 附录结构占位文件 `parts/appendix.tex`、`parts/appendix-survey.tex`、`parts/appendix-translation.tex`

---

## 重要修改点

### 修改封面和基础信息
编辑 `Info.tex`，修改封面信息、学校、导师、题目等内容即可生成自己的论文封面。

### 调整字体与行间距
如果需要自定义字体，可在 `gduptbe.cls` 中修改字体加载逻辑，或在 `Info.tex` 中启用 `fontspec`、`setCJKmainfont` 等配置。

### 更改参考文献格式
目前默认使用 `gbt7714`，如果需要不同格式，可修改 `gduptbe.cls` 或替换为其他 BibTeX 样式文件。

---

## 编译建议
- 使用 `XeLaTeX` 编译；`pdfLaTeX` 不支持本模板的中文和 `fontspec` 设置。
- 参考文献建议使用 `BibTeX`：`bibtex thesis`
- 先编译一次 `XeLaTeX`，再运行 `BibTeX`，然后再编译两次 `XeLaTeX`。
- 若使用 VS Code + LaTeX Workshop，请确保 `latexmk` 或 `texify` 调用了 `xelatex`。

---

## 常见问题
- 如果出现“`XeLaTeX is required`”错误，说明当前编译器不是 `XeLaTeX`。
- 如果中文字体不能显示，请安装常用中文字体（如 `SimSun`、`STSong`、`STKaiti`）。
- 如果图片无法显示，确认 `imgs/` 或 `figs/` 中图片路径与 `thesis.tex` 中引用路径一致。

---

## 参考资料
本项目基于广东石油化工学院本科论文模板，并参考 `phd-thesis-template`、`thuthesis` 等开源模板。
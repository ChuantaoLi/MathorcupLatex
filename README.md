# MathorCup LaTex 模板

基于 Andrew82106 开源的模板 [MathorcupLatexTemplate](https://github.com/Andrew82106/MathorcupLatexTemplate) 修改，编译器选用 XeLaTeX，主要修改：

- 删除 newtxmath, esint, amsfonts, amsthm，保留 amsmath, amssymb；移除 physics, siunitx；删除 zhlipsum, mwe，试图解决原来模板在 Overleaf 上编译超时的问题。但如果插入图片比较多，还是会超时......
- 修改了页码的显示，从“第x页 共x页”修改为“x”；修改了参考文献的显示和编号，且字号比正文字号小一号；修改了论文标题的字号和字体，看起来大一些醒目一些。
- 修复了参考文献章节在目录中格式不正确的问题，修改为和其他一级标题一样的样式。

无论是在 Overleaf 还是本地编译，都需要先将编译器设置为 XeLaTeX，否则会导致编译错误。在本地可以通过以下指令进行编译：

```bash
xelatex -C
xelatex Manuscript.tex
```

本地编译LaTex的时候，因为默认是pdflatex编译器，所以Ctrl+S保存的默认编译会在该模板上报错。如果不去settings.json中设置，可以直接在.tex首行添加：

```bash
% !TEX program = xelatex
```

如果这时候Ctrl+S可以正常编译，但页底的页码、正文超链接跳转以及目录无法正常显示，再编译一次即可解决。
